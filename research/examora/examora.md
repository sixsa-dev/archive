**Analisis Mekanisme Keamanan Examora**

**1. Pembangunan Token Awal (ec1 & ec2)**
Saat inisialisasi aplikasi, komponen native (libnativelib.so) membangun dua token unik:
- **ec1**: Mengandung base URL dan path endpoint (contoh: `https://api.examora.id/app/xxx`)
- **ec2**: Mengandung query parameter token (contoh: `?pathToken=yyy`)

Kedua token ini dihasilkan dari kombinasi timestamp, device fingerprint, dan konstanta yang di-hardcode di memori native (masih belum terpecahkan).

**2. Konstruksi Request URL**
Aplikasi mengkompilasi URL lengkap dengan menggabungkan:
- Base URL dari `ec1`
- Path token dari `ec2`
- Token ujian yang diinput oleh pengguna

Format akhir:  
`https://api.examora.id/app/[ec1_path]?pathToken=[ec2_token]&examToken=[token_ujian]`

**3. Server Response Structure**
Server merespons dengan struktur JSON:
```json
{
  "success": true,
  "message": "",
  "data": {
    "examData": {
      "examTitle": "string",
      "examUrl": "https://forms.gle/...",
      "isAudioEnabled": boolean,
      "isExitOnEnd": boolean,
      "examStartTime": 1773022200000, // Timestamp (ms)
      "examEndTime": 1773026100000,   // Timestamp (ms)
      "backupToken": "null",
      "backupTokenTimeMinutes": null,
      "temporaryEndTime": null
    }
  }
}
```

**4. Enforcement Mechanism**

*Kasus 1: Token Reuse Detection*
- Sistem memonitor setiap request ke endpoint
- Jika terdeteksi penggunaan kombinasi `examToken` + `ec1`/`ec2` yang sama untuk request kedua
- Server merespons dengan HTTP 403 dan meminta `backupToken`

*Kasus 2: First Violation*
- Saat sistem mendeteksi anomali (root detection, emulator, debugger)
- Server meminta `backupToken` melalui endpoint khusus
- Aplikasi harus mengirim `examToken` + `backupToken` untuk mendapatkan sesi baru
- Server mereset state dan memberikan token baru

*Kasus 3: Persistent Violation*
- Jika terjadi pelanggaran kedua (misal: force exit saat ujian berlangsung)
- Aplikasi menulis flag ke persistent storage (`/data/data/[package]/...`)
- Flag ini bersifat persisten dan tidak hilang meskipun app di-restart
- **Namun**: Jika data aplikasi di-reset (clear data), flag akan terhapus dan pengguna dapat memulai sesi baru

**5. Unverified Behavior**
- Belum diketahui apakah setelah menggunakan `backupToken` (Kasus 2) dan kemudian melakukan pelanggaran lagi, server akan:
  - Opsi A: Menolak kedua token (`examToken` dan `backupToken`)
  - Opsi B: Kembali meminta `backupToken` baru (loop mechanism)

**Kesimpulan Sementara**
Sistem menggunakan pendekatan token berlapis dengan state machine di sisi server. Deteksi kecurangan bersifat progresif: peringatan → backup token → persistent flag. Kelemahan potensial terletak pada persistent flag yang dapat di-reset melalui clear data aplikasi.
Tentu! Berikut adalah materi dasar Python yang **difokuskan dari awal sampai Input**, disusun dengan bahasa yang santai dan mudah dipahami seperti sedang belajar langsung bersama teman.

---

# 🐍 Dasar-Dasar Python: Dari Nol sampai Bisa Input
**Level:** Pemula Mutlak  
**Fokus:** Memahami cara komputer menyimpan dan membaca data.

---

## 1. Pengenalan Singkat: Apa itu Python?
Bayangkan Python adalah **bahasa pengantar** antara kamu dan komputer. 
- Komputer hanya mengerti angka 0 dan 1.
- Manusia mengerti bahasa sehari-hari.
- **Python** adalah jembatan yang membuat kita bisa memberi perintah ke komputer menggunakan bahasa yang mirip bahasa Inggris sederhana.

**Kelebihan Python:**
- Mudah dibaca (tidak banyak simbol aneh).
- Populer (banyak dipakai di Google, Netflix, Instagram).
- Serbaguna (bisa buat web, analisis data, AI, dll).

---

## 2. Cara Menjalankan Kode
Sebelum mulai, kamu butuh tempat untuk menulis kode. Ada dua cara mudah:

1.  **Online (Tanpa Install):** Buka website seperti [Programiz Online Python](https://www.programiz.com/python-programming/online-compiler/) atau [Replit](https://replit.com/). Kamu bisa langsung ketik dan jalankan di browser.
2.  **Offline (Install di Laptop):** Install Python dari `python.org` dan gunakan aplikasi seperti **VS Code**.

*Untuk belajar awal, saran saya pakai **Online Compiler** dulu agar tidak ribet instalasi.*

---

## 3. Perintah Output: `print()`
Ini adalah perintah paling dasar. Gunanya untuk **menampilkan sesuatu ke layar**. Bayangkan ini seperti komputer "berbicara" kepada kamu.

```python
print("Halo, selamat pagi!")
print(100)
```

**Penjelasan:**
- `print` adalah perintahnya.
- Tanda kurung `()` adalah tempat kamu memasukkan apa yang ingin ditampilkan.
- Tanda kutip `""` digunakan jika yang ingin ditampilkan adalah **teks**.
- Jika yang ditampilkan **angka**, tidak perlu tanda kutip.

**Hasil di Layar:**
```text
Halo, selamat pagi!
100
```

---

## 4. Variabel: Kotak Penyimpanan
Dalam pemrograman, kita butuh tempat untuk menyimpan data agar bisa dipakai nanti. Tempat ini disebut **Variabel**.

**Analogi:**
Bayangkan variabel seperti **kardus bekas**.
1.  Kamu punya kardus.
2.  Kamu beri label nama pada kardus itu (misal: `nama`).
3.  Kamu isi kardus itu dengan sesuatu (misal: `"Budi"`).

**Contoh Kode:**
```python
nama = "Andi"
umur = 25
tinggi = 170.5

print(nama)
print(umur)
```

**Penjelasan:**
- `nama`, `umur`, `tinggi` adalah **label kardus** (nama variabel).
- `=` adalah tanda **isi kardus ini dengan...** (bukan sama dengan matematika).
- `"Andi"` adalah **isi kardusnya**.
- Saat kita `print(nama)`, komputer akan melihat isi kardus berlabel `nama` dan menampilkannya.

**Aturan Penamaan Variabel:**
- ✅ `nama_saya` (Boleh)
- ✅ `namaSaya` (Boleh)
- ❌ `1nama` (Salah, tidak boleh dimulai angka)
- ❌ `print` (Salah, jangan pakai nama perintah bawaan)

---

## 5. Tipe Data: Jenis Isi Kotak
Komputer perlu tahu jenis data apa yang ada di dalam variabel agar tidak salah olah. Ada 4 jenis utama yang wajib kamu tahu:

| Tipe Data | Nama di Python | Contoh | Keterangan |
| :--- | :--- | :--- | :--- |
| **Teks** | `string` (`str`) | `"Halo"`, `'Budi'` | Harus pakai tanda kutip. |
| **Bilangan Bulat** | `integer` (`int`) | `10`, `50`, `-5` | Angka tanpa koma. |
| **Bilangan Desimal** | `float` | `3.14`, `2.5` | Angka pakai koma (titik). |
| **Logika** | `boolean` (`bool`) | `True`, `False` | Hanya benar atau salah. |

**Contoh Cek Tipe Data:**
Kamu bisa bertanya pada Python, "Ini tipe data apa?" menggunakan `type()`.

```python
x = 10
y = "Sepuluh"

print(type(x))  # Output: <class 'int'>
print(type(y))  # Output: <class 'str'>
```

---

## 6. Operator: Alat Hitung
Variabel bisa diolah menggunakan operator. Yang paling sering dipakai adalah **Operator Aritmatika** (Matematika).

```python
a = 10
b = 3

print(a + b)   # Penjumlahan -> 13
print(a - b)   # Pengurangan -> 7
print(a * b)   # Perkalian -> 30
print(a / b)   # Pembagian -> 3.333...
print(a // b)  # Pembagian Bulat -> 3 (koma dibuang)
print(a % b)   # Modulus (Sisa Bagi) -> 1 (karena 10 dibagi 3 sisanya 1)
print(a ** b)  # Pangkat -> 1000 (10 pangkat 3)
```

**Tips:** Urutan operasi matematika tetap berlaku (perkalian dikerjakan sebelum penjumlahan).

---

## 7. Perintah Input: Bertanya pada User
Jika `print` adalah komputer berbicara ke kamu, maka `input` adalah **komputer mendengarkan kamu**.

**Contoh Kode:**
```python
nama = input("Siapa nama kamu? ")
print("Halo,", nama)
```

**Cara Kerjanya:**
1.  Program berjalan sampai baris `input`.
2.  Program **BERHENTI** dan menunggu kamu mengetik sesuatu di keyboard lalu tekan Enter.
3.  Setelah Enter, apa yang kamu ketik akan disimpan ke dalam variabel `nama`.
4.  Program lanjut ke baris `print`.

### ⚠️ PERINGATAN PENTING (Jebakan Pemula)
Secara default, **hasil dari `input()` selalu dianggap TEKS (String)**, meskipun kamu mengetik angka.

**Contoh Masalah:**
```python
angka1 = input("Masukkan angka 1: ")  # User ketik: 10
angka2 = input("Masukkan angka 2: ")  # User ketik: 5

hasil = angka1 + angka2
print(hasil)
```
**Output yang muncul:** `105` (Bukan 15!)  
**Kenapa?** Karena komputer menganggap itu teks, jadi dia menggabungkan teks "10" dan "5" menjadi "105".

### ✅ Solusi: Type Casting (Mengubah Tipe Data)
Jika ingin menghitung angka dari input, kamu harus mengubahnya dari **Teks** menjadi **Angka (int)** dulu.

```python
angka1 = int(input("Masukkan angka 1: "))  # Dibungkus int()
angka2 = int(input("Masukkan angka 2: "))  # Dibungkus int()

hasil = angka1 + angka2
print("Hasil penjumlahan:", hasil)
```
**Output sekarang:** `15` (Benar!)

- Gunakan `int()` untuk bilangan bulat.
- Gunakan `float()` untuk bilangan desimal (koma).

---

## 8. Studi Kasus: Program Biodata Sederhana
Mari gabungkan semua materi di atas (Print, Variabel, Input, Operator) menjadi satu program kecil.

**Tujuan:** Membuat program yang menanyakan nama, tahun lahir, lalu menghitung umur.

```python
# 1. Minta input data dari user
nama = input("Masukkan nama lengkap: ")
tahun_lahir = input("Masukkan tahun lahir: ")
tahun_sekarang = 2024

# 2. Olah data (Hitung umur)
# Ingat! tahun_lahir harus diubah jadi angka (int) dulu
umur = tahun_sekarang - int(tahun_lahir)

# 3. Tampilkan hasil
print("--- Hasil Biodata ---")
print("Nama:", nama)
print("Tahun Lahir:", tahun_lahir)
print("Umur Anda adalah:", umur, "tahun")
```

**Contoh Jalannya Program:**
```text
Masukkan nama lengkap: Siti
Masukkan tahun lahir: 2000
--- Hasil Biodata ---
Nama: Siti
Tahun Lahir: 2000
Umur Anda adalah: 24 tahun
```

---

## 9. Rangkuman & Tips Hafalan

1.  **`print()`**: Untuk menampilkan sesuatu ke layar.
2.  **Variabel**: Tempat menyimpan data (seperti kardus berlabel).
3.  **`input()`**: Untuk menerima data dari user. Hasilnya selalu **teks**.
4.  **`int()` / `float()`**: Wajib dipakai jika ingin menghitung angka dari input user.
5.  **`#`**: Digunakan untuk membuat **komentar** (catatan untuk programmer, tidak dibaca komputer).

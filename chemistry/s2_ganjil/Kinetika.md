# ⚗️ Laju Reaksi & Kinetika Kimia

> 📚 *Ringkasan materi kinetika kimia: laju reaksi, hukum laju, dan metode penentuannya.*

---

## 📋 Daftar Isi

- [⚗️ Laju Reaksi \& Kinetika Kimia](#️-laju-reaksi--kinetika-kimia)
  - [📋 Daftar Isi](#-daftar-isi)
  - [🔬 Konsep Dasar](#-konsep-dasar)
  - [⚖️ Termodinamika vs Kinetika](#️-termodinamika-vs-kinetika)
  - [📈 Ekspresi Laju Reaksi](#-ekspresi-laju-reaksi)
    - [🔁 Contoh Perhitungan](#-contoh-perhitungan)
  - [🧮 Laju Rata-rata \& Sesaat](#-laju-rata-rata--sesaat)
    - [📉 Laju Rata-rata (Average Rate)](#-laju-rata-rata-average-rate)
    - [🎯 Laju Sesaat (Instantaneous Rate)](#-laju-sesaat-instantaneous-rate)
  - [📐 Hukum Laju \& Orde Reaksi](#-hukum-laju--orde-reaksi)
    - [Bentuk Umum Hukum Laju:](#bentuk-umum-hukum-laju)
    - [Arti Eksponen (Orde):](#arti-eksponen-orde)
    - [🎯 Contoh:](#-contoh)
  - [🔍 Metode Laju Awal (Initial Rates Method)](#-metode-laju-awal-initial-rates-method)
    - [Langkah-langkah:](#langkah-langkah)
    - [📊 Contoh Data Eksperimen:](#-contoh-data-eksperimen)
      - [🔎 Analisis:](#-analisis)
      - [✅ Hasil:](#-hasil)
  - [🧪 Konstanta Laju (k)](#-konstanta-laju-k)
    - [Rumus:](#rumus)
    - [📐 Satuan k Bergantung pada Orde Total:](#-satuan-k-bergantung-pada-orde-total)
    - [🔢 Contoh Perhitungan:](#-contoh-perhitungan-1)
  - [📊 Tabel Ringkasan Orde Reaksi](#-tabel-ringkasan-orde-reaksi)
  - [💡 Insight Penting](#-insight-penting)
  - [🧩 Contoh](#-contoh-1)
    - [Soal 1:](#soal-1)
    - [Soal 2:](#soal-2)
  - [🔗 Referensi \& Lanjutan](#-referensi--lanjutan)

---

## 🔬 Konsep Dasar

| Istilah | Definisi |
|---------|----------|
| **Kinetika Kimia** | Studi tentang laju reaksi dan seberapa cepat reaksi berlangsung. |
| **Termodinamika** | Mempelajari apakah reaksi spontan atau menguntungkan secara energi, *bukan* kecepatannya. |
| **Laju Reaksi** | Perubahan konsentrasi reaktan atau produk per satuan waktu. |
| **Hukum Laju** | Persamaan yang menyatakan laju reaksi sebagai fungsi konsentrasi reaktan: `Rate = k[A]ˣ[B]ʸ` |
| **Orde Reaksi** | Eksponen pada hukum laju yang menunjukkan sensitivitas laju terhadap konsentrasi reaktan. |
| **Orde Reaksi Total** | Jumlah semua eksponen orde dari masing-masing reaktan. |

---

## ⚖️ Termodinamika vs Kinetika

```
❓ Mengapa intan tidak berubah menjadi grafit meskipun spontan?
❓ Mengapa glukosa tidak terbakar spontan di udara kamar?

✅ Jawaban: KINETIKA!
```

| Aspek | Termodinamika | Kinetika |
|-------|--------------|----------|
| **Fokus** | Apakah reaksi *bisa* terjadi? | Seberapa *cepat* reaksi terjadi? |
| **Parameter** | ΔG, ΔH, ΔS | Laju, energi aktivasi, mekanisme |
| **Contoh** | Pembakaran glukosa: spontan (ΔG < 0) | Tapi butuh percikan api untuk memulai (Eₐ tinggi) |

> 💡 Reaksi bisa **spontan secara termodinamika**, tapi **sangat lambat secara kinetika** karena energi aktivasi tinggi.

---

## 📈 Ekspresi Laju Reaksi

Untuk reaksi umum:  
`aA + bB → cC + dD`

Laju reaksi dinyatakan terhadap masing-masing spesies:

| Spesies | Ekspresi Laju | Keterangan |
|---------|--------------|------------|
| **A** | `-1/a · Δ[A]/Δt` | Reaktan: tanda negatif |
| **B** | `-1/b · Δ[B]/Δt` | Reaktan: tanda negatif |
| **C** | `+1/c · Δ[C]/Δt` | Produk: tanda positif |
| **D** | `+1/d · Δ[D]/Δt` | Produk: tanda positif |

### 🔁 Contoh Perhitungan

Diketahui:  
`2A + 3B → 4C`  
Laju disappearance B = `0.6 M/s`

Maka:
```
Laju reaksi = -1/3 · Δ[B]/Δt = 0.6/3 = 0.2 M/s

Laju appearance C = +1/4 · Δ[C]/Δt = 0.2 M/s
→ Δ[C]/Δt = 0.2 × 4 = 0.8 M/s ✅
```

---

## 🧮 Laju Rata-rata & Sesaat

### 📉 Laju Rata-rata (Average Rate)
```
Rate_avg = -Δ[A]/Δt = -([A]₂ - [A]₁) / (t₂ - t₁)
```
- Dihitung dari perubahan konsentrasi dalam interval waktu tertentu.
- Sama dengan **gradien garis sekan** pada grafik [A] vs t.

### 🎯 Laju Sesaat (Instantaneous Rate)
- Dihitung dari **gradien garis singgung** pada kurva [A] vs t pada waktu tertentu.
- Lebih akurat untuk menggambarkan laju pada momen spesifik.

```python
# Ilustrasi konsep (pseudo-code)
t = [0, 10, 20, 30]          # waktu (s)
[A] = [1.0, 0.8, 0.6, 0.4]   # konsentrasi (M)

# Laju rata-rata 0→20s:
rate_avg = -(0.6 - 1.0) / (20 - 0) = 0.02 M/s

# Laju sesaat di t=10s:
# → hitung gradien tangent pada titik tersebut
```

---

## 📐 Hukum Laju & Orde Reaksi

### Bentuk Umum Hukum Laju:
```
Rate = k [A]ˣ [B]ʸ [C]ᶻ ...
```

### Arti Eksponen (Orde):

| Orde | Efek jika [Reaktan] dilipatgandakan 2x | Hubungan Matematis |
|------|----------------------------------------|-------------------|
| **0** (nol) | Laju tetap (×1) | Rate ∝ [A]⁰ = konstan |
| **1** (pertama) | Laju ×2 | Rate ∝ [A]¹ |
| **2** (kedua) | Laju ×4 | Rate ∝ [A]² |
| **3** (ketiga) | Laju ×8 | Rate ∝ [A]³ |

### 🎯 Contoh:
Jika `Rate = k [A]¹ [B]²`:
- Orde terhadap A = 1 → doubling [A] → laju ×2
- Orde terhadap B = 2 → doubling [B] → laju ×4
- **Orde total** = 1 + 2 = **3**

---

## 🔍 Metode Laju Awal (Initial Rates Method)

### Langkah-langkah:
1. Lakukan eksperimen dengan variasi konsentrasi **satu reaktan**, sementara lainnya tetap.
2. Bandingkan perubahan laju terhadap perubahan konsentrasi.
3. Gunakan rumus logaritmik untuk mencari orde:

```
x = log(Rate₂/Rate₁) / log([A]₂/[A]₁)
```

### 📊 Contoh Data Eksperimen:

| Eksperimen | [A] (M) | [B] (M) | Laju Awal (M/s) |
|------------|---------|---------|-----------------|
| 1 | 0.10 | 0.10 | 0.020 |
| 2 | 0.20 | 0.10 | 0.040 |
| 3 | 0.10 | 0.20 | 0.080 |

#### 🔎 Analisis:
- **Eksperimen 1 → 2**: [A] ×2, [B] tetap, Laju ×2  
  → Orde terhadap A = **1**
  
- **Eksperimen 1 → 3**: [B] ×2, [A] tetap, Laju ×4  
  → Orde terhadap B = **2** (karena 2² = 4)

#### ✅ Hasil:
```
Hukum laju: Rate = k [A]¹ [B]²
Orde total = 1 + 2 = 3
```

---

## 🧪 Konstanta Laju (k)

### Rumus:
```
k = Rate / ([A]ˣ [B]ʸ)
```

### 📐 Satuan k Bergantung pada Orde Total:

| Orde Total | Satuan k (jika Rate dalam M/s) |
|------------|-------------------------------|
| 0 | M·s⁻¹ |
| 1 | s⁻¹ |
| 2 | M⁻¹·s⁻¹ atau L·mol⁻¹·s⁻¹ |
| 3 | M⁻²·s⁻¹ atau L²·mol⁻²·s⁻¹ |
| n | M¹⁻ⁿ·s⁻¹ |

### 🔢 Contoh Perhitungan:
Diketahui:
- Rate = 0.040 M/s
- [A] = 0.20 M, [B] = 0.10 M
- Hukum laju: `Rate = k [A]¹ [B]²`

```
k = 0.040 / (0.20¹ × 0.10²)
  = 0.040 / (0.20 × 0.01)
  = 0.040 / 0.002
  = 20

Satuan: M/s ÷ (M¹ × M²) = M⁻²·s⁻¹ = L²·mol⁻²·s⁻¹
→ k = 20 L²·mol⁻²·s⁻¹ ✅
```

---

## 📊 Tabel Ringkasan Orde Reaksi

| Orde Reaktan | Jika [Reaktan] ×2 | Jika [Reaktan] ×3 | Persamaan Laju |
|--------------|-------------------|-------------------|----------------|
| **0** | Laju ×1 (tetap) | Laju ×1 | Rate = k |
| **1** | Laju ×2 | Laju ×3 | Rate = k[A] |
| **2** | Laju ×4 | Laju ×9 | Rate = k[A]² |
| **3** | Laju ×8 | Laju ×27 | Rate = k[A]³ |

> 🎯 **Tips**: Untuk menentukan orde, cari pola:  
> `(Perubahan laju) = (Perubahan konsentrasi)ᵒʳᵈᵉ`

---

## 💡 Insight Penting

✅ **Hukum laju ditentukan secara eksperimen**, *bukan* dari koefisien stoikiometri.  
✅ **Tanda negatif** pada reaktan memastikan laju reaksi selalu bernilai positif.  
✅ **Satuan k** harus konsisten dengan orde total — selalu cek dimensi!  
✅ **Metode laju awal** adalah cara paling andal untuk menentukan orde reaksi.  
✅ **Reaktan orde nol** tidak memengaruhi laju, meskipun konsentrasinya diubah.  
✅ **Orde lebih tinggi** = pengaruh konsentrasi lebih besar terhadap laju (efek eksponensial).  

---

## 🧩 Contoh

### Soal 1:
Diketahui reaksi `A + 2B → C` memiliki hukum laju `Rate = k[A]²[B]`.  
Jika [A] dilipatgandakan 3x dan [B] dilipatgandakan 2x, berapa kali laju berubah?

<details>
<summary>💡 Klik untuk jawaban</summary>

```
Rate baru / Rate lama = (3)² × (2)¹ = 9 × 2 = 18
→ Laju meningkat 18 kali lipat ✅
```
</details>

### Soal 2:
Satuan k untuk reaksi orde total 3 adalah...?

<details>
<summary>💡 Klik untuk jawaban</summary>

```
Rate = M/s
[A]³ = M³
k = Rate / [A]³ = (M/s) / M³ = M⁻²·s⁻¹ = L²·mol⁻²·s⁻¹ ✅
```
</details>

---

## 🔗 Referensi & Lanjutan
- https://www.youtube.com/watch?v=oh4L2gcI5ds)
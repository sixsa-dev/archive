```markdown
# 🐍 Panduan Lengkap Belajar Pemrograman Python

> **Bahasa:** Indonesia  
> **Tingkat:** Pemula hingga Menengah  
> **Versi Python:** 3.x

---

## 📋 Daftar Isi

1. [Bab 1: Pengenalan & Persiapan](#bab-1-pengenalan--persiapan)
2. [Bab 2: Variabel & Tipe Data](#bab-2-variabel--tipe-data)
3. [Bab 3: Operator & Input/Output](#bab-3-operator--inputoutput)
4. [Bab 4: Struktur Kontrol](#bab-4-struktur-kontrol)
5. [Bab 5: Struktur Data](#bab-5-struktur-data)
6. [Bab 6: Fungsi](#bab-6-fungsi)
7. [Bab 7: Penanganan Error & File](#bab-7-penanganan-error--file)
8. [Bab 8: OOP](#bab-8-pemrograman-berorientasi-objek-oop)
9. [Bab 9: Modul & Library](#bab-9-modul--pustaka-library)
10. [Bab 10: Proyek Akhir](#bab-10-proyek-akhir-studi-kasus)

---

## Bab 1: Pengenalan & Persiapan

### 1.1 Apa itu Python?

Python adalah bahasa pemrograman **tingkat tinggi** yang:
- ✅ Mudah dibaca (syntax mirip bahasa Inggris)
- ✅ Serbaguna (web, data science, AI, automation)
- ✅ Open source & komunitas besar
- ✅ Multi-platform (Windows, Linux, macOS)

### 1.2 Instalasi

```bash
# 1. Download dari python.org
# 2. Saat instalasi, CENTANG "Add Python to PATH"
# 3. Verifikasi instalasi:
python --version
pip --version
```

### 1.3 Program Pertama: Hello World

```python
# hello.py
print("👋 Halo, Dunia!")
print("🚀 Selamat belajar Python!")
```

**Menjalankan kode:**
```bash
python hello.py
```

**Output:**
```
👋 Halo, Dunia!
🚀 Selamat belajar Python!
```

---

## Bab 2: Variabel & Tipe Data

### 2.1 Variabel

```python
# Deklarasi variabel (tanpa tipe eksplisit)
nama = "Budi"           # str
umur = 25               # int
tinggi = 170.5          # float
is_active = True        # bool
data_kosong = None      # NoneType

print(f"{nama}, {umur} tahun")  # f-string (Python 3.6+)
```

### 2.2 Tipe Data Dasar

| Tipe Data | Contoh | Deskripsi |
|-----------|--------|-----------|
| `int` | `10`, `-5`, `0` | Bilangan bulat |
| `float` | `3.14`, `2.0`, `-0.5` | Bilangan desimal |
| `str` | `"Halo"`, `'Python'` | Teks/string |
| `bool` | `True`, `False` | Nilai logika |
| `None` | `None` | Nilai kosong/null |

### 2.3 Cek & Konversi Tipe Data

```python
# Cek tipe data
print(type(umur))  # <class 'int'>

# Konversi tipe data (type casting)
angka_str = "100"
angka_int = int(angka_str)      # str → int: 100
angka_float = float(angka_str)  # str → float: 100.0
teks = str(2024)                # int → str: "2024"
```

---

## Bab 3: Operator & Input/Output

### 3.1 Operator Aritmatika

```python
a, b = 10, 3

print(a + b)   # 13  → Penjumlahan
print(a - b)   # 7   → Pengurangan
print(a * b)   # 30  → Perkalian
print(a / b)   # 3.333... → Pembagian (float)
print(a // b)  # 3   → Pembagian bulat (floor)
print(a % b)   # 1   → Modulus (sisa bagi)
print(a ** b)  # 1000 → Pangkat
```

### 3.2 Operator Perbandingan & Logika

```python
x, y = 5, 10

# Perbandingan
print(x > y)    # False
print(x == y)   # False
print(x != y)   # True
print(x <= 5)   # True

# Logika
print(x > 3 and y < 20)  # True  (AND)
print(x > 3 or y < 2)    # True  (OR)
print(not(x > 3))        # False (NOT)
```

### 3.3 Input & Output

```python
# Input dari user (selalu string)
nama = input("📛 Nama Anda: ")
umur = int(input("🎂 Umur Anda: "))  # Konversi ke int

# Output dengan format
print(f"✨ Halo {nama}, umur {umur} tahun!")

# Output multiple
print("Python", "itu", "keren", sep=" 🐍 ")
print("Baris 1", end=" | ")
print("Baris 2")
```

---

## Bab 4: Struktur Kontrol

### 4.1 Percabangan: If-Elif-Else

```python
nilai = 80

if nilai >= 90:
    grade = "A"
    predikat = "Sangat Baik"
elif nilai >= 75:
    grade = "B"
    predikat = "Baik"
elif nilai >= 60:
    grade = "C"
    predikat = "Cukup"
else:
    grade = "D"
    predikat = "Perlu Improvisasi"

print(f"Grade: {grade} ({predikat})")
```

### 4.2 Perulangan: For Loop

```python
# Range dasar
for i in range(5):          # 0,1,2,3,4
    print(f"Iterasi ke-{i}")

# Range dengan start & stop
for i in range(2, 6):       # 2,3,4,5
    print(i)

# Range dengan step
for i in range(0, 10, 2):   # 0,2,4,6,8
    print(f"Genap: {i}")

# Loop melalui list
buah = ["🍎 Apel", "🍊 Jeruk", "🥭 Mangga"]
for item in buah:
    print(f"- {item}")

# Loop dengan index (enumerate)
for idx, item in enumerate(buah, start=1):
    print(f"{idx}. {item}")
```

### 4.3 Perulangan: While Loop

```python
# Counter dasar
count = 0
while count < 5:
    print(f"Count: {count}")
    count += 1  # ⚠️ Jangan lupa increment!

# Loop dengan break & continue
angka = 0
while True:
    angka += 1
    if angka % 2 == 0:
        continue  # Lewati angka genap
    print(f"Odd: {angka}")
    if angka >= 10:
        break     # Keluar dari loop
```

### 4.4 Kontrol Loop

| Keyword | Fungsi |
|---------|--------|
| `break` | Menghentikan loop secara paksa |
| `continue` | Melewati iterasi saat ini, lanjut ke berikutnya |
| `pass` | Placeholder (tidak melakukan apa-apa) |

---

## Bab 5: Struktur Data

### 5.1 List (Mutable, Ordered)

```python
# Membuat list
buah = ["Apel", "Pisang", "Cherry"]

# Akses elemen
print(buah[0])      # "Apel" (index dari 0)
print(buah[-1])     # "Cherry" (index dari belakang)

# Modifikasi
buah[1] = "Jeruk"           # Ubah nilai
buah.append("Mangga")       # Tambah di akhir
buah.insert(1, "Kiwi")      # Sisip di index tertentu
buah.extend(["Anggur"])     # Tambah multiple

# Hapus elemen
buah.remove("Cherry")       # Hapus berdasarkan nilai
item = buah.pop()           # Hapus & kembalikan elemen terakhir
del buah[0]                 # Hapus berdasarkan index

# Operasi list
print(len(buah))            # Panjang list
print("Jeruk" in buah)      # Cek keberadaan: True/False

# Slicing [start:stop:step]
angka = [0,1,2,3,4,5]
print(angka[1:4])   # [1,2,3]
print(angka[::2])   # [0,2,4]
print(angka[::-1])  # [5,4,3,2,1,0] → reverse
```

### 5.2 Tuple (Immutable, Ordered)

```python
# Membuat tuple
koordinat = (10, 20)
warna_rgb = (255, 128, 0)

# Akses (sama seperti list)
print(koordinat[0])  # 10

# ⚠️ Tidak bisa dimodifikasi
# koordinat[0] = 5  → TypeError!

# Tuple unpacking
x, y = koordinat
print(f"x={x}, y={y}")

# Single element tuple (perlu koma)
single = ("hanya satu",)
```

### 5.3 Dictionary (Key-Value, Mutable)

```python
# Membuat dictionary
mahasiswa = {
    "nama": "Andi",
    "nim": "12345",
    "ipk": 3.8,
    "matkul": ["Algoritma", "Basis Data"]
}

# Akses nilai
print(mahasiswa["nama"])           # "Andi"
print(mahasiswa.get("email"))      # None (aman, tidak error)
print(mahasiswa.get("email", "N/A"))  # "N/A" (default value)

# Modifikasi & tambah
mahasiswa["ipk"] = 3.9             # Update nilai
mahasiswa["email"] = "andi@edu.com"  # Tambah key baru

# Operasi dictionary
print("nim" in mahasiswa)          # True
print(mahasiswa.keys())            # Daftar key
print(mahasiswa.values())          # Daftar value
print(mahasiswa.items())           # Daftar (key, value)

# Loop dictionary
for key, value in mahasiswa.items():
    print(f"{key}: {value}")

# Hapus elemen
del mahasiswa["matkul"]
email = mahasiswa.pop("email")
```

### 5.4 Set (Unordered, Unique)

```python
# Membuat set
angka = {1, 2, 3, 3, 4}  # Duplikat otomatis dihapus
print(angka)  # {1, 2, 3, 4}

# Operasi set
a = {1, 2, 3}
b = {3, 4, 5}

print(a | b)   # Union: {1, 2, 3, 4, 5}
print(a & b)   # Intersection: {3}
print(a - b)   # Difference: {1, 2}
print(a ^ b)   # Symmetric difference: {1, 2, 4, 5}

# Metode set
angka.add(5)           # Tambah elemen
angka.update([6, 7])   # Tambah multiple
angka.remove(3)        # Hapus (error jika tidak ada)
angka.discard(10)      # Hapus (aman, tidak error)
```

---

## Bab 6: Fungsi

### 6.1 Definisi & Pemanggilan Fungsi

```python
def sapa(nama, waktu="Pagi"):
    """
    Fungsi untuk menyapa pengguna.
    
    Args:
        nama (str): Nama pengguna
        waktu (str): Waktu sapaan (default: "Pagi")
    
    Returns:
        str: Kalimat sapaan
    """
    return f"Selamat {waktu}, {nama}! 👋"

# Pemanggilan
print(sapa("Budi"))                    # Selamat Pagi, Budi! 👋
print(sapa("Siti", waktu="Malam"))     # Selamat Malam, Siti! 👋
```

### 6.2 Parameter: *args & **kwargs

```python
# *args → menerima multiple positional arguments (tuple)
def jumlahkan(*angka):
    return sum(angka)

print(jumlahkan(1, 2, 3))      # 6
print(jumlahkan(10, 20, 30, 40))  # 100

# **kwargs → menerima multiple keyword arguments (dict)
def profil(**data):
    for key, value in data.items():
        print(f"{key}: {value}")

profil(nama="Andi", umur=25, kota="Jakarta")
```

### 6.3 Lambda Function (Fungsi Anonim)

```python
# Syntax: lambda parameter: ekspresi
kuadrat = lambda x: x ** 2
print(kuadrat(5))  # 25

# Gunakan dengan fungsi higher-order
angka = [1, 2, 3, 4, 5]
genap = list(filter(lambda x: x % 2 == 0, angka))
print(genap)  # [2, 4]

# Sorting dengan lambda
mahasiswa = [
    {"nama": "Budi", "ipk": 3.5},
    {"nama": "Ani", "ipk": 3.9},
]
# Urutkan berdasarkan IPK descending
mahasiswa_sorted = sorted(mahasiswa, key=lambda x: x["ipk"], reverse=True)
```

### 6.4 Scope Variabel

```python
x = "global"  # Global scope

def fungsi_luar():
    y = "enclosing"  # Enclosing scope
    
    def fungsi_dalam():
        z = "local"  # Local scope
        print(x, y, z)
    
    fungsi_dalam()

fungsi_luar()
# print(z)  # ❌ Error: z tidak dikenal di luar fungsi_dalam
```

---

## Bab 7: Penanganan Error & File

### 7.1 Exception Handling: Try-Except

```python
try:
    angka = int(input("Masukkan angka: "))
    hasil = 10 / angka
    print(f"Hasil: {hasil}")
    
except ValueError:
    print("❌ Error: Input harus angka!")
    
except ZeroDivisionError:
    print("❌ Error: Tidak bisa dibagi nol!")
    
except Exception as e:
    print(f"❌ Error tak terduga: {e}")
    
else:
    print("✅ Operasi berhasil!")
    
finally:
    print("🔚 Program selesai.")
```

### 7.2 Raise Exception Kustom

```python
def cek_umur(umur):
    if umur < 0:
        raise ValueError("Umur tidak boleh negatif!")
    if umur < 17:
        raise PermissionError("Harus 17+ untuk akses ini!")
    return "Akses diizinkan ✅"

try:
    cek_umur(15)
except Exception as e:
    print(f"⚠️ {type(e).__name__}: {e}")
```

### 7.3 Operasi File

```python
# ✍️ Menulis file (mode: w = write, a = append)
with open("catatan.txt", "w", encoding="utf-8") as file:
    file.write("📝 Catatan Harian\n")
    file.write("- Belajar Python\n")
    file.write("- Olahraga pagi\n")

# 📖 Membaca file (mode: r = read)
with open("catatan.txt", "r", encoding="utf-8") as file:
    isi = file.read()           # Baca seluruh isi
    print(isi)

# 📖 Baca per baris
with open("catatan.txt", "r", encoding="utf-8") as file:
    for baris in file:
        print(f"→ {baris.strip()}")  # strip() hapus newline

# 📋 Mode file lainnya:
# "r"  → read (default)
# "w"  → write (hapus isi lama)
# "a"  → append (tambah di akhir)
# "x"  → create (error jika file sudah ada)
# "b"  → binary mode
# "t"  → text mode (default)
# "r+" → read + write
```

---

## Bab 8: Pemrograman Berorientasi Objek (OOP)

### 8.1 Class & Object Dasar

```python
class Mahasiswa:
    # Class variable (shared by all instances)
    universitas = "Universitas Python"
    
    # Constructor / Inisialisasi
    def __init__(self, nama, nim, jurusan):
        # Instance variables
        self.nama = nama
        self.nim = nim
        self.jurusan = jurusan
        self.ipk = 0.0
    
    # Instance method
    def tampilkan_profil(self):
        return f"{self.nama} ({self.nim}) - {self.jurusan}"
    
    def update_ipk(self, ipk_baru):
        if 0.0 <= ipk_baru <= 4.0:
            self.ipk = ipk_baru
            return True
        return False
    
    # Magic method / Dunder method
    def __str__(self):
        return f"🎓 {self.nama} | IPK: {self.ipk}"

# Membuat object / instance
mhs1 = Mahasiswa("Budi", "12345", "Informatika")
mhs1.update_ipk(3.75)

print(mhs1.tampilkan_profil())  # Budi (12345) - Informatika
print(mhs1)                      # 🎓 Budi | IPK: 3.75
print(Mahasiswa.universitas)     # Universitas Python
```

### 8.2 Inheritance (Pewarisan)

```python
# Parent class
class Hewan:
    def __init__(self, nama):
        self.nama = nama
    
    def bersuara(self):
        return "..."

# Child class
class Kucing(Hewan):
    def bersuara(self):  # Method overriding
        return "Meong! 🐱"
    
    def makan(self):
        return f"{self.nama} makan ikan."

class Anjing(Hewan):
    def bersuara(self):
        return "Guk guk! 🐶"

# Penggunaan
kucing = Kucing("Mochi")
anjing = Anjing("Bingo")

print(kucing.bersuara())  # Meong! 🐱
print(kucing.makan())     # Mochi makan ikan.
print(anjing.bersuara())  # Guk guk! 🐶

# Cek inheritance
print(isinstance(kucing, Kucing))  # True
print(isinstance(kucing, Hewan))   # True
```

### 8.3 Encapsulation & Property

```python
class RekeningBank:
    def __init__(self, pemilik, saldo_awal=0):
        self._pemilik = pemilik      # Protected (konvensi)
        self.__saldo = saldo_awal    # Private (name mangling)
    
    # Getter
    @property
    def saldo(self):
        return self.__saldo
    
    # Setter dengan validasi
    @saldo.setter
    def saldo(self, nilai):
        if nilai >= 0:
            self.__saldo = nilai
        else:
            raise ValueError("Saldo tidak boleh negatif!")
    
    def deposit(self, jumlah):
        if jumlah > 0:
            self.__saldo += jumlah
            return True
        return False
    
    def tarik(self, jumlah):
        if 0 < jumlah <= self.__saldo:
            self.__saldo -= jumlah
            return True
        return False

# Penggunaan
rek = RekeningBank("Andi", 100000)
print(rek.saldo)        # 100000 (via property)
rek.deposit(50000)
rek.tarik(30000)
print(rek.saldo)        # 120000
```
---

## 📚 Sumber Belajar Lanjutan

### 🌐 Dokumentasi & Referensi
- [🐍 Python Official Docs](https://docs.python.org/3/)
- [📖 W3Schools Python](https://www.w3schools.com/python/)
- [🧪 Real Python Tutorials](https://realpython.com/)

### 💻 Platform Latihan
| Platform | Fokus | Link |
|----------|-------|------|
| HackerRank | Algoritma | [hackerrank.com](https://www.hackerrank.com/) |
| LeetCode | Interview Prep | [leetcode.com](https://leetcode.com/) |
| Codewars | Challenge Fun | [codewars.com](https://www.codewars.com/) |
| Exercism | Mentored Practice | [exercism.org](https://exercism.org/) |

### 🎥 Video Tutorial (Bahasa Indonesia)
- [Kelas Terbuka - YouTube](https://youtube.com/c/KelasTerbuka)
- [Programmer Zaman Now - YouTube](https://youtube.com/c/ProgrammerZamanNow)
- [Web Programming UNPAS - YouTube](https://youtube.com/c/WebProgrammingUNPAS)


---

## Bab 9: Modul & Pustaka (Library)

### 9.1 Import Modul Bawaan

```python
# Import seluruh modul
import math
import random
import datetime
import json
import os

# Import spesifik
from math import sqrt, pi
from datetime import datetime, timedelta

# Contoh penggunaan
print(f"√16 = {sqrt(16)}")                    # 4.0
print(f"π = {pi}")                            # 3.14159...
print(f"Acak 1-100: {random.randint(1, 100)}")
print(f"Sekarang: {datetime.now().strftime('%Y-%m-%d %H:%M')}")

# JSON: serialize & deserialize
data = {"nama": "Budi", "umur": 25}
json_str = json.dumps(data, indent=2)  # Dict → JSON string
print(json_str)

parsed = json.loads(json_str)          # JSON string → Dict
print(parsed["nama"])                  # "Budi"
```

### 9.2 Install & Gunakan Paket Eksternal (pip)

```bash
# Install package
pip install requests
pip install pandas numpy matplotlib

# Install versi tertentu
pip install flask==2.3.0

# Lihat package terinstall
pip list

# Update package
pip install --upgrade requests

# Hapus package
pip uninstall nama_package
```

```python
# Contoh: requests untuk HTTP
import requests

response = requests.get("https://api.github.com")
if response.status_code == 200:
    data = response.json()
    print(data)

# Contoh: pandas untuk data analysis
import pandas as pd

df = pd.DataFrame({
    "Nama": ["Budi", "Siti", "Andi"],
    "Umur": [25, 30, 22],
    "Kota": ["Jakarta", "Bandung", "Surabaya"]
})
print(df)
print(df[df["Umur"] > 23])  # Filter
```

### 9.3 Membuat Modul Sendiri

```python
# file: utils.py
def format_rupiah(angka):
    return f"Rp {angka:,.0f}".replace(",", ".")

def is_even(n):
    return n % 2 == 0

# file: main.py
from utils import format_rupiah, is_even

print(format_rupiah(1500000))  # Rp 1.500.000
print(is_even(10))             # True
```

---

## Bab 10: Proyek Akhir - To-Do List CLI

```python
"""
📋 Aplikasi To-Do List Sederhana
Fitur: Tambah, Lihat, Hapus, Simpan ke File
"""

import json
import os

FILE_DB = "todo_db.json"

def load_data():
    """Load data dari file JSON"""
    if not os.path.exists(FILE_DB):
        return []
    with open(FILE_DB, "r", encoding="utf-8") as f:
        return json.load(f)

def save_data(data):
    """Simpan data ke file JSON"""
    with open(FILE_DB, "w", encoding="utf-8") as f:
        json.dump(data, f, indent=2, ensure_ascii=False)

def tambah_tugas(data):
    """Tambah tugas baru"""
    tugas = input("✨ Nama tugas: ").strip()
    if tugas:
        data.append({"id": len(data)+1, "tugas": tugas, "selesai": False})
        save_data(data)
        print("✅ Tugas ditambahkan!")
    else:
        print("⚠️ Tugas tidak boleh kosong!")

def lihat_tugas(data):
    """Tampilkan semua tugas"""
    if not data:
        print("📭 Tidak ada tugas.")
        return
    
    print("\n📋 DAFTAR TUGAS:")
    print("-" * 40)
    for item in data:
        status = "✅" if item["selesai"] else "⏳"
        print(f"{item['id']}. [{status}] {item['tugas']}")
    print("-" * 40)

def hapus_tugas(data):
    """Hapus tugas berdasarkan ID"""
    try:
        idx = int(input("🗑️  ID tugas yang dihapus: "))
        for i, item in enumerate(data):
            if item["id"] == idx:
                removed = data.pop(i)
                save_data(data)
                print(f"✅ '{removed['tugas']}' dihapus!")
                return
        print("❌ ID tidak ditemukan!")
    except ValueError:
        print("❌ Input harus angka!")

def toggle_selesai(data):
    """Tandai tugas sebagai selesai/belum"""
    try:
        idx = int(input("🔄 ID tugas: "))
        for item in data:
            if item["id"] == idx:
                item["selesai"] = not item["selesai"]
                status = "✅ SELESAI" if item["selesai"] else "⏳ BELUM"
                save_data(data)
                print(f"🔄 Status: {status}")
                return
        print("❌ ID tidak ditemukan!")
    except ValueError:
        print("❌ Input harus angka!")

def main():
    """Fungsi utama aplikasi"""
    data = load_data()
    
    while True:
        print("\n" + "🎯 TO-DO LIST APP ".center(40, "="))
        print("1. 📋 Lihat Tugas")
        print("2. ➕ Tambah Tugas")
        print("3. 🔄 Tandai Selesai")
        print("4. 🗑️  Hapus Tugas")
        print("5. 🚪 Keluar")
        print("=" * 40)
        
        pilihan = input("Pilih menu (1-5): ").strip()
        
        if pilihan == "1":
            lihat_tugas(data)
        elif pilihan == "2":
            tambah_tugas(data)
        elif pilihan == "3":
            toggle_selesai(data)
        elif pilihan == "4":
            hapus_tugas(data)
        elif pilihan == "5":
            print("👋 Terima kasih! Sampai jumpa!")
            break
        else:
            print("⚠️ Pilihan tidak valid!")

if __name__ == "__main__":
    main()
```


<p align="center">
  <a href="https://putusan3.mahkamahagung.go.id/direktori.html"><img src="https://img.shields.io/badge/sumber-Mahkamah%20Agung%20RI-8b0000?style=flat-square" alt="Sumber Data"></a>
  <a href="https://sipp.pn-kisaran.go.id"><img src="https://img.shields.io/badge/satker-PN%20Kisaran-1f4e78?style=flat-square" alt="Pengadilan Negeri Kisaran"></a>
  <img src="https://img.shields.io/badge/klasifikasi-Pidana%20Khusus%20Narkotika-2e7d32?style=flat-square" alt="Klasifikasi">
  <img src="https://img.shields.io/badge/dokumen-5%20Putusan%20(131%20Halaman)-455a64?style=flat-square" alt="Jumlah Dokumen">
  <img src="https://img.shields.io/badge/format-PDF%20%26%20XLSX-5c6bc0?style=flat-square" alt="Format">
</p>

## Tentang Dataset

Repositori ini berisi kumpulan dokumen putusan pengadilan tingkat pertama untuk perkara tindak pidana khusus narkotika yang diambil dari [Direktori Putusan Mahkamah Agung RI](https://putusan3.mahkamahagung.go.id/direktori.html). Seluruh dokumen dalam dataset ini berasal dari satu satuan kerja pengadilan yang sama, yaitu **Pengadilan Negeri Kisaran (PN Kis)** di bawah wilayah hukum Pengadilan Tinggi Medan.

Dataset ini disusun untuk kebutuhan tugas mata kuliah **Temu Kembali Informasi (Information Retrieval)** Semester Ganjil 2026/2027 di Program Studi Informatika, Universitas Muhammadiyah Malang. Fokus utamanya adalah mengumpulkan dokumen putusan asli berformat PDF yang belum berstatus berkekuatan hukum tetap pada metadata direktori, lalu memetakan informasi intinya (nomor perkara, lembaga peradilan, rincian barang bukti, dan diktum amar putusan) ke dalam format tabel terstruktur.

Meskipun hanya terdiri dari lima berkas putusan sebagai sampel akuisisi manual, kasus yang tercakup di dalamnya punya rentang karakteristik perkara narkotika yang cukup lebar di PN Kisaran:
- **Penyalahgunaan bagi diri sendiri (Pasal 127 ayat (1) huruf a UU Narkotika):** Barang bukti sabu netto 0,79 gram beserta alat hisap (*bong* dan kaca *pirex*) dengan vonis 1 tahun penjara (`91/Pid.Sus/2025/PN Kis`).
- **Kepemilikan dan penguasaan narkotika (Pasal 112 ayat (1) dan ayat (2) UU Narkotika):** Mulai dari kepemilikan paket kecil dengan vonis 4 tahun penjara (`462/Pid.Sus/2023/PN Kis`) hingga penguasaan dua paket sabu total netto 10,68 gram dengan vonis 8 tahun penjara (`456/Pid.Sus/2024/PN Kis`).
- **Turut serta membeli narkotika (Pasal 114 ayat (2) Jo. Pasal 55 ayat (1) ke-1 KUHP):** Pembelian sabu netto 29,50 gram dengan vonis 7 tahun penjara, di mana barang bukti kendaraan dikembalikan kepada saksi pemilik (`440/Pid.Sus/2026/PN Kis`).
- **Permufakatan jahat peredaran jaringan besar (Pasal 114 ayat (2) Jo. Pasal 132 ayat (1) UU Narkotika):** Perkara tiga terdakwa dengan barang bukti 20 bungkus teh China *Guanyinwang* berisi sabu seberat netto 20.000 gram (20 kg), yang berujung pada vonis pidana mati bagi dua terdakwa dan penjara seumur hidup bagi satu terdakwa, disertai perampasan kendaraan dan uang tunai untuk negara (`724/Pid.Sus/2025/PN Kis`).

## Anggota Kelompok

- **Anggota 1:** Fakhar Hanif (202310370311127)

## Struktur Direktori Repositori

```text
Dataset-Narkotika_127/
├── Dataset/
│   ├── Narkotika.zip        # Arsip 5 dokumen putusan sampel manual (Sub-CPMK 2)
│   ├── PDF/                 # 77 dokumen putusan asli berformat .pdf hasil web crawling (Sub-CPMK 3 & 4)
│   └── TXT/                 # 77 dokumen teks putusan bersih berformat .txt (Sub-CPMK 3 & 4)
├── Overview/
│   ├── Overview.xlsx        # Tabel ringkasan 5 putusan sampel manual (Sub-CPMK 2)
│   └── hasil_ekstraksi_77_putusan_pn_kisaran.csv  # Tabel hasil ekstraksi otomatis 77 putusan (Sub-CPMK 3)
└── README.md
```

## Daftar Berkas di Dalam `Dataset/Narkotika.zip`

Seluruh berkas PDF di dalam `Narkotika.zip` merupakan dokumen digital asli (*born-digital PDF*, *producer* `FPDF 1.81`) yang diunduh langsung dari server Kepaniteraan Mahkamah Agung RI tanpa modifikasi isi teks.

| No | Nama Berkas di Dalam ZIP | Nomor Putusan | Tanggal Putusan | Halaman | Ukuran |
| :-: | :--- | :--- | :--- | :-: | --: |
| 1 | `putusan_462_pid.sus_2023_pn_kis_20261105225244.pdf` | `462/Pid.Sus/2023/PN Kis` | 31 Juli 2023 | 15 | 130 KB |
| 2 | `putusan_456_pid.sus_2024_pn_kis_20261105225207.pdf` | `456/Pid.Sus/2024/PN Kis` | 14 Agustus 2024 | 19 | 167 KB |
| 3 | `putusan_91_pid.sus_2025_pn_kis_20261105225516.pdf` | `91/Pid.Sus/2025/PN Kis` | 19 Maret 2025 | 20 | 148 KB |
| 4 | `putusan_724_pid.sus_2025_pn_kis_20261105225422.pdf` | `724/Pid.Sus/2025/PN Kis` | 12 November 2025 | 61 | 344 KB |
| 5 | `putusan_440_pid.sus_2026_pn_kis_20261106015443.pdf` | `440/Pid.Sus/2026/PN Kis` | 20 Agustus 2026 | 16 | 206 KB |

## Struktur Kolom `Overview/Overview.xlsx`

Berkas `Overview/Overview.xlsx` merekapitulasi isi pokok dari kelima dokumen putusan ke dalam lima kolom:

| Kolom | Penjelasan |
| :--- | :--- |
| `No` | Nomor urut data (1 sampai 5). |
| `No Putusan` | Nomor registrasi perkara di Pengadilan Negeri Kisaran (contoh: `456/Pid.Sus/2024/PN Kis`). |
| `Lembaga Peradilan` | Nama lembaga peradilan tingkat pertama yang memutus perkara (`PN Kisaran`). |
| `Barang Bukti` | Daftar lengkap barang bukti yang tercantum pada diktum penetapan barang bukti di bagian amar putusan, dipisahkan per butir item. |
| `Amar Putusan` | Teks utuh dari diktum putusan majelis hakim yang berada di bawah subjudul `MENGADILI:`, mencakup pernyataan bersalah, lama pidana penjara, besaran denda beserta ketentuan subsidair, status penahanan, perlakuan terhadap barang bukti, dan pembebanan biaya perkara. |

### Cuplikan Isi Tabel Overview

| No | No Putusan | Lembaga Peradilan | Terdakwa | Ringkasan Barang Bukti | Ringkasan Vonis (Amar) |
| :-: | :--- | :--- | :--- | :--- | :--- |
| 1 | `462/Pid.Sus/2023/PN Kis` | PN Kisaran | Supriadi Als Supri | 3 paket kecil sabu; 1 tas sandang coklat | Terbukti tanpa hak memiliki Narkotika Gol. I bukan tanaman; penjara 4 tahun, denda Rp1,2 miliar subsidair 1 bulan penjara; barang bukti dimusnahkan. |
| 2 | `456/Pid.Sus/2024/PN Kis` | PN Kisaran | Ahmad Fauzi Als Uzi | 1 plastik klip besar sabu (brutto 8,80 g / netto 8,34 g); 1 plastik klip sedang sabu (brutto 2,62 g / netto 2,34 g); 1 kotak rokok Surya; 1 HP Samsung | Terbukti tanpa hak menguasai Narkotika Gol. I bukan tanaman > 5 gram; penjara 8 tahun, denda Rp1 miliar subsidair 3 bulan penjara; barang bukti dimusnahkan. |
| 3 | `91/Pid.Sus/2025/PN Kis` | PN Kisaran | Nasri | 2 paket plastik klip sabu (brutto 1,37 g / netto 0,79 g); 1 kaca pirex; 1 bong; 1 mancis | Bebas dari dakwaan primair; terbukti dakwaan subsidair penyalahguna Narkotika Gol. I bagi diri sendiri; penjara 1 tahun; barang bukti dimusnahkan. |
| 4 | `724/Pid.Sus/2025/PN Kis` | PN Kisaran | Rudi Kesuma Sitorus, Robi, Irwansyah | 20 bungkus teh China *Guanyinwang* berisi sabu (brutto 20.725,5 g / netto 20.000 g); 1 karung plastik; 3 unit HP; 1 mobil Wuling BK 1304 JD + STNK & kunci; uang Rp4.000.000 | Terbukti permufakatan jahat tanpa hak menyerahkan Narkotika Gol. I bukan tanaman > 5 gram; Terdakwa I & II pidana mati, Terdakwa III penjara seumur hidup; sabu & HP dimusnahkan, mobil & uang dirampas untuk negara. |
| 5 | `440/Pid.Sus/2026/PN Kis` | PN Kisaran | Patar Simanjuntak | 1 plastik transparan berisi sabu (bruto 30,32 g / neto 29,50 g); 1 sepeda motor Honda CB 150 R silver tanpa nopol | Terbukti tanpa hak turut serta membeli Narkotika Gol. I; penjara 7 tahun; sabu dimusnahkan, sepeda motor dikembalikan kepada saksi Erwin Simanjuntak. |

## Catatan Teknis Karakteristik Teks PDF Putusan MA

Bagi yang ingin memakai dataset ini untuk eksperimen *text preprocessing*, *parsing*, atau *indexing* di Python, ada beberapa pola bawaan PDF Direktori Putusan MA yang perlu diperhatikan:

1. **Artefak Watermark & Header Halaman:** Setiap pergantian halaman di PDF terbitan MA menyisipkan potongan teks *watermark* berulang seperti `hkama`, `ahkamah Agung Repub`, `mah Agung Republik Indonesia`, serta baris header `Direktori Putusan Mahkamah Agung Republik Indonesia / putusan.mahkamahagung.go.id`. Teks ini perlu dibersihkan dengan *regular expression* sebelum tahap tokenisasi agar tidak mengotori *term frequency*.
2. **Blok Disclaimer di Kaki Halaman:** Di setiap bagian bawah halaman terdapat kotak *Disclaimer* Kepaniteraan MA RI beserta nomor telepon dan email (`kepaniteraan@mahkamahagung.go.id`) yang sering memotong kalimat amar atau pertimbangan hakim yang menyambung ke halaman berikutnya.
3. **Batas Seksi Amar Putusan:** Diktum amar selalu diawali kata kunci `MENGADILI:` (atau `M E N G A D I L I :`) dan ditutup dengan kalimat `Demikian diputuskan dalam sidang permusyawaratan Majelis Hakim...` atau `Demikianlah diputuskan...`. Rincian barang bukti di dalam amar selalu diawali frasa `Menetapkan barang bukti berupa:`.

## Contoh Membaca Dataset dengan Python

Berikut contoh skrip singkat menggunakan `pandas` dan `PyMuPDF` (`pymupdf`) untuk memuat tabel ringkasan sekaligus mengekstrak teks bersih dari arsip `Dataset/Narkotika.zip`:

```python
import re
import zipfile
import pandas as pd
import pymupdf

# 1. Baca ringkasan dari Overview.xlsx
df = pd.read_excel("Overview/Overview.xlsx")
print(df[["No", "No Putusan", "Lembaga Peradilan"]])

# 2. Baca teks tiap PDF langsung dari dalam Narkotika.zip tanpa perlu ekstrak manual
with zipfile.ZipFile("Dataset/Narkotika.zip", "r") as zf:
    for filename in zf.namelist():
        raw_bytes = zf.read(filename)
        doc = pymupdf.open(stream=raw_bytes, filetype="pdf")
        full_text = "\n".join(page.get_text() for page in doc)

        # Bersihkan artefak watermark & footer halaman MA
        clean_text = re.sub(r"Disclaimer[\s\S]*?Halaman \d+\s*", "", full_text)
        clean_text = re.sub(
            r"^(hkama|ahkamah|mah Agung|blik Indonesi|Direktori Putusan|putusan\.mahkamahagung).*$",
            "",
            clean_text,
            flags=re.MULTILINE,
        )
        print(f"{filename} -> {len(doc)} halaman, {len(clean_text):,} karakter bersih")
```

## Lisensi & Keterbukaan Informasi

Seluruh dokumen putusan pengadilan di dalam repositori ini bersumber dari publikasi resmi Mahkamah Agung Republik Indonesia berdasarkan **UU No. 14 Tahun 2008 tentang Keterbukaan Informasi Publik** dan **SK Ketua Mahkamah Agung RI No. 1-144/KMA/SK/I/2011** tentang Pedoman Pelayanan Informasi di Pengadilan. Dokumen putusan pengadilan merupakan dokumen publik negara yang bersifat terbuka, tidak terikat Hak atas Kekayaan Intelektual (HaKI), dan disusun di repositori ini khusus untuk keperluan pendidikan serta riset akademik.

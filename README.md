# Dashboard Perwujudan Tata Ruang Kota Blitar 2025

Website dashboard interaktif berbasis HTML, CSS, JavaScript, dan Chart.js untuk menampilkan Matriks Hasil Penilaian Perwujudan Kota Blitar Tahun 2025.

## Fitur
- Filter kategori, waktu, instansi pelaksana, program, dan pencarian.
- KPI serta ringkasan otomatis mengikuti filter.
- Donut chart status, bar chart keterwujudan program, grafik periode, dan frekuensi instansi.
- Tampilan terpisah untuk rekap program utama dan detail Inprog.
- Reset filter, ekspor CSV yang dapat dibuka dengan Excel, serta cetak/simpan PDF dari browser.
- Responsif untuk desktop dan perangkat seluler.

## Sumber data dan definisi
Data di folder `data/` diekstrak dari workbook **Matriks Hasil Penilaian Perwujudan Kota Blitar Tahun 2025**, dengan dua sheet:
- **Perwujudan Struktur**: 34 record yang memiliki kategori, terdiri dari 29 `Terwujud` dan 5 `Belum Terwujud`.
- **Perwujudan Inprog Struktur**: 184 record yang memiliki kategori, terdiri dari 177 `Sudah Terwujud` dan 7 `Belum Terwujud`.

Kedua tabel sengaja dipisahkan karena unit analisis berbeda dan tidak dijumlahkan. Persentase rekap dinormalisasi ke angka 0–1 untuk grafik; teks persentase dari sumber tetap ditampilkan di tabel. Angka sumber `1.0` pada satu record diperlakukan sebagai 100% dalam visualisasi. Rata-rata pada KPI adalah rata-rata aritmetika sederhana, bukan indeks resmi berbobot. Nilai kosong tidak diimputasi.

Grafik instansi memecah daftar beberapa instansi dalam satu sel berdasarkan baris baru, koma, dan titik koma. Satu program dapat memiliki beberapa instansi sehingga frekuensi instansi dapat melebihi jumlah record program.

### Koreksi hitungan awal
Pemeriksaan ulang langsung pada workbook asli menghasilkan 34 record rekap berstatus (29/5), bukan 31 record (26/5) dari ekstraksi awal Power BI. Gunakan angka situs ini untuk tinjauan ulang dan konfirmasikan dengan pemilik data sebelum dinyatakan sebagai capaian resmi.

## Mengaktifkan GitHub Pages
1. Buka repository **Settings** → **Pages**.
2. Di **Build and deployment**, pilih **Deploy from a branch**.
3. Pilih branch `main` dan folder `/(root)`, lalu klik **Save**.
4. Tunggu sampai GitHub menampilkan status publikasi. URL situs:  
   https://hazidien.github.io/DASHBOARD-PERWUJUDAN-TATA-RUANG/

Jika Pages belum aktif, pemilik/admin repository harus mengaktifkannya. Browser perlu koneksi internet karena Chart.js dimuat dari CDN.

## Privasi
Repository ini publik. Seluruh file dalam folder `data/` dapat diakses siapa pun, termasuk rincian program dan lokasi yang tercantum pada workbook. Pastikan instansi/pemilik data mengizinkan publikasi sebelum mengirimkan URL kepada khalayak luas. Untuk data internal, gunakan platform dengan autentikasi, bukan GitHub Pages publik.

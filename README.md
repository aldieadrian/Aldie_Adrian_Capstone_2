# Aldie_Adrian_Capstone_2
Capstone Modul 2 - Analisis Transaksi Transjakarta

# Analisis Data Transjakarta

## Latar Belakang

Transjakarta merupakan salah satu moda transportasi umum utama di Jakarta, Indonesia, yang menawarkan layanan bus cepat transisi. Dalam proyek ini, kita menganalisis dataset Transjakarta untuk mengidentifikasi peluang optimalisasi tarif yang bertujuan untuk meningkatkan pendapatan tanpa mengurangi aksesibilitas atau kepuasan pengguna.

## Tujuan

Tujuan dari analisis ini adalah untuk:
1. Mengidentifikasi pola penggunaan Transjakarta, termasuk jam sibuk dan koridor populer.
2. Meninjau distribusi tarif saat ini dan demografi pengguna untuk mengidentifikasi peluang penyesuaian tarif.
3. Mengusulkan rekomendasi tarif baru yang berpotensi meningkatkan pendapatan Transjakarta.

## Dataset

Dataset ini terdiri dari dua file CSV: `Transjakarta.csv` yang belum dibersihkan dan `Transjakarta_clean.csv` yang merupakan hasil dari proses pembersihan data. Setiap record dalam dataset mencakup informasi mengenai transaksi perjalanan penumpang, termasuk ID transaksi, informasi kartu pembayaran, koridor, titik tap-in dan tap-out, serta tarif yang dibayarkan.

## Proses Pembersihan Data

Proses pembersihan data meliputi beberapa langkah utama:

### Check In Bus
- Identifikasi dan penghapusan entri duplikat dan entri dengan nilai yang hilang pada kolom penting seperti `corridorID`, `corridorName`, dan `tapInStops`.
- Pembuatan pemetaan berdasarkan `tapInStopsName`, `tapInStopsLat`, `tapInStopsLon`, untuk mengisi nilai yang hilang pada `corridorID`, `corridorName`, dan `tapInStops`.

### Check Out Bus
- Pengisian nilai yang hilang untuk `tapOutStops` berdasarkan informasi lokasi dan nama halte yang tersedia.
- Penghapusan record yang masih memiliki nilai yang hilang setelah proses pengisian, untuk menjaga keakuratan data.

### Analisis Data

Analisis data meliputi:
- **Distribusi Tarif**: Peninjauan seberapa sering masing-masing tarif dibayarkan oleh penumpang.
- **Demografi Pengguna**: Analisis jenis kelamin dan kelompok umur pengguna untuk mengidentifikasi segmen pengguna.
- **Jam Sibuk dan Koridor Populer**: Identifikasi waktu dan koridor dengan volume penggunaan tertinggi untuk menargetkan penyesuaian tarif.
- **Pola Perjalanan**: Analisis rute-rute populer berdasarkan titik tap-in dan tap-out untuk mengidentifikasi potensi penyesuaian tarif.

## Rekomendasi

Berdasarkan analisis, kami mengusulkan beberapa rekomendasi untuk optimalisasi tarif, termasuk implementasi tarif dinamis selama jam sibuk, pengenalan tarif berbasis jarak, dan program diskon target untuk segmen pengguna tertentu.

## Kesimpulan

Analisis data Transjakarta ini menawarkan wawasan berharga tentang cara meningkatkan pendapatan melalui penyesuaian strategis tarif, dengan tetap mempertimbangkan keseimbangan antara permintaan dan kepuasan pengguna. Dengan mengimplementasikan rekomendasi ini, Transjakarta dapat meningkatkan pendapatan sambil mempertahankan layanan yang aksesibel dan memuaskan bagi penggunanya.

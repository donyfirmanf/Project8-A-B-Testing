# Project8-A-B-Testing

## Deskripsi Proyek

### Konteks

Anda adalah seorang analis di sebuah toko daring besar. Anda bersama tim pemasaran telah menyusun daftar hipotesis untuk membantu meningkatkan pendapatan.

Anda perlu memprioritaskan hipotesis tersebut, menjalankan *A/B testing*, dan menganalisis hasilnya.

## Deskripsi Data

**Data yang digunakan pada bagian pertama proyek**

`/datasets/hypotheses_us.csv` [Unduh *dataset*](https://code.s3.yandex.net/datasets/hypotheses_us.csv)

- `Hypotheses` — deskripsi singkat tentang hipotesis
- `Reach` — jangkauan pengguna, dalam skala satu hingga sepuluh
- `Impact` — dampak terhadap pengguna, dalam skala satu hingga sepuluh
- `Confidence` — keyakinan pada hipotesis, dalam skala satu sampai sepuluh
- `Effort` — sumber daya yang diperlukan untuk menguji hipotesis, dalam skala satu sampai sepuluh. Semakin tinggi nilai `Effort`, semakin intensif sumber daya pengujiannya.

**Data yang digunakan pada bagian kedua proyek**

`/datasets/orders_us.csv` [Unduh *dataset*](https://code.s3.yandex.net/datasets/orders_us.csv)

- `transactionId` — ID pesanan
- `visitorId` — ID pengguna yang membuat pesanan
- `date` — tanggal dibuatnya pesanan
- `revenue` — pendapatan dari pesanan
- `group` — kelompok uji (*test group*) A/B tempat pengguna berada

`/datasets/visits_us.csv` [Unduh *dataset*](https://code.s3.yandex.net/datasets/visits_us.csv)

- `date` — tanggal
- `group` — kelompok uji (*test group*) A/B
- `visits` — jumlah kunjungan pada tanggal yang ditentukan untuk kelompok uji A/B yang ditentukan

Pastikan untuk melakukan pra-pemrosesan data terlebih dahulu. Tidak menutup kemungkinan, *dataset* asli yang Anda miliki mengandung kesalahan; misalnya, sebagian pengunjung mungkin berada di kelompok A maupun di kelompok B.

### Bagian 1. Memprioritaskan Hipotesis

*File* `hypotheses_us.csv` memuat sembilan hipotesis untuk meningkatkan pendapatan toko daring dengan `Reach`, `Impact`, `Confidence`, dan `Effort` yang sudah ditentukan untuk masing-masing hipotesis.

Tugas Anda adalah:

- Menerapkan *framework* `ICE` untuk memprioritaskan hipotesis. Urutkan hipotesis tersebut dalam urutan prioritas menurun.
- Menerapkan *framework* `RICE` untuk memprioritaskan hipotesis. Urutkan hipotesis tersebut dalam urutan prioritas menurun.
- Menunjukkan perubahan prioritas hipotesis saat `RICE` diterapkan untuk menggantikan `ICE`. Berikan penjelasan terkait perubahan tersebut.

### Bagian 2. Analisis *A/B Testing*

Anda telah melakukan *A/B testing* dan mendapatkan hasil seperti yang dideskripsikan dalam *file*  `orders_us.csv` dan `visits_us.csv`.

**Soal**

Menganalisis *A/B testing*:

1. Gambarkan pendapatan kumulatif berdasarkan kelompok. Buatlah kesimpulan dan asumsinya.
2. Gambarkan ukuran pesanan rata-rata kumulatif berdasarkan kelompok. Buatlah kesimpulan dan asumsinya.
3. Gambarkan perbedaan relatif untuk ukuran pesanan rata-rata kumulatif kelompok B yang dibandingkan dengan kelompok A. Buatlah kesimpulan dan asumsinya.
4. Hitung tingkat konversi setiap kelompok sebagai rasio pesanan terhadap jumlah kunjungan setiap hari. Buat grafik tingkat konversi harian dari kedua kelompok dan jelaskan perbedaannya. Buatlah kesimpulan dan asumsinya.
5. Buatlah diagram tebar (*scatter chart*) untuk jumlah pesanan per pengguna. Buatlah kesimpulan dan asumsinya.
6. Hitung persentil ke-95 dan ke-99 untuk jumlah pesanan per pengguna. Tentukan titik ketika suatu titik data berubah menjadi anomali.
7. Buatlah diagram tebar (*scatter chart*) untuk harga pesanan. Buatlah kesimpulan dan asumsinya.
8. Hitung persentil ke-95 dan ke-99 untuk harga pesanan. Tentukan titik ketika suatu titik data berubah menjadi anomali.
9. Temukan signifikansi statistik perbedaan konversi antar kelompok menggunakan data mentah. Buatlah kesimpulan dan asumsinya.
10. Temukan signifikansi statistik perbedaan ukuran pesanan rata-rata antar kelompok menggunakan data mentah. Buatlah kesimpulan dan asumsinya.
11. Temukan signifikansi statistik perbedaan konversi antar kelompok menggunakan data yang telah difilter. Buatlah kesimpulan dan asumsinya.
12. Temukan signifikansi statistik perbedaan ukuran pesanan rata-rata antar kelompok menggunakan data yang telah difilter. Buatlah kesimpulan dan asumsinya.
13. Buatlah keputusan berdasarkan hasil pengujian. Keputusan yang memungkinkan adalah:
    1. Menghentikan pengujian, serta mempertimbangkan salah satu kelompok sebagai pemimpin.
    2. Menghentikan pengujian, serta menyimpulkan bahwa tidak ada perbedaan antara kedua kelompok.
    3. Melanjutkan pengujian.

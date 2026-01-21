# Analisis Klasterisasi Kabupaten/Kota di Sumatera Barat Berdasarkan Indikator Sosio-Ekonomi

Proyek ini bertujuan untuk mengidentifikasi pola pembangunan wilayah di Provinsi Sumatera Barat dengan mengelompokkan kabupaten dan kota berdasarkan karakteristik ketenagakerjaan dan tingkat pendidikan menggunakan teknik *Machine Learning* (Unsupervised Learning).

## Deskripsi Proyek
Analisis ini menggunakan metode **K-Means Clustering** yang dioptimalkan dengan **Principal Component Analysis (PCA)** untuk memetakan wilayah-wilayah di Sumatera Barat dan menggunakan metode **Hierarchical Clustering** juga untuk melihat konsistensi hasil klastering. Fokus utama penelitian ini adalah melihat hubungan antara tingkat pendidikan dan kondisi pasar kerja (pengangguran).

## Indikator yang Digunakan
Data yang dianalisis mencakup periode 2017-2024 dengan empat variabel kunci:
1.  **Tingkat Pengangguran Terbuka (TPT):** Persentase angkatan kerja yang tidak bekerja.
2.  **Tingkat Partisipasi Angkatan Kerja (TPAK):** Persentase penduduk usia kerja yang aktif secara ekonomi.
3.  **Tingkat Setengah Pengangguran:** Pekerja dengan jam kerja kurang dari normal.
4.  **Rata-rata Lama Sekolah (RLS):** Indikator tingkat pendidikan penduduk.

## Metodologi & Alur Kerja
Proyek ini mengikuti langkah-langkah *Data Science* standar:
- **Eksplorasi Data (EDA):** Visualisasi distribusi data dan korelasi antar variabel.
- **Preprocessing:** Standardisasi data menggunakan `StandardScaler`.
- **Reduksi Dimensi:** Menggunakan PCA untuk menyederhanakan fitur tanpa kehilangan informasi penting.
- **Klasterisasi:** Penentuan jumlah klaster optimal melalui *Elbow Method* dan Evaluasi model dengan *Silhouette Score* dan *Davies-Bouldin Index*.
- **Visualisasi Hierarki:** Pembuatan Dendrogram untuk melihat kedekatan antar wilayah.

## Hasil Analisis
Berdasarkan hasil pemodelan, wilayah di Sumatera Barat terbagi menjadi dua klaster utama:

### **Klaster 1:**
* **Karakteristik:** Secara numerik, klaster ini dicirikan oleh kombinasi TPAK tinggi, setengah pengangguran tinggi, dan rata-rata lama sekolah relatif rendah, dengan dominasi wilayah administrasi berbentuk kabupaten.
* **Wilayah:** Kab. Agam, Kab. Dharmasraya, Kab. Kepulauan Mentawai, Kab. Lima Puluh Kota, Kab. Padang Pariaman, Kab. Pasaman, Kab. Pasaman Barat, Kab. Pesisir Selatan, Kab. Sijunjung, Kab. Solok, Kab. Solok Selatan dan Kab. Tanah Datar

### **Klaster 2:**
* **Karakteristik:** Secara numerik, klaster ini dicirikan oleh rata-rata lama sekolah tinggi, pengangguran terbuka relatif tinggi, dan setengah pengangguran lebih rendah, dengan dominasi wilayah perkotaan.
* **Wilayah:** Kota Bukittinggi, Kota Padang, Kota Padang Panjang, Kota Pariaman, Kota Payakumbuh, Kota Sawahlunto dan Kota Solok.

## Teknologi yang Digunakan
* **Bahasa:** Python
* **Libraries:** - `pandas` & `numpy` (Manipulasi Data)
    - `matplotlib` & `seaborn` (Visualisasi)
    - `scikit-learn` (Machine Learning & PCA)
    - `scipy` (Statistik & Hierarchical Clustering)

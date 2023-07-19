## Laporan Akhir Kecerdasan Buatan - Kelompok 7



**Anggota Kelompok :**

1. Rangga Prabaswara - NIM. 3.34.21.0.21

2. Wahyu Indra Permana - NIM. 3.34.21.0.23

   

## Domain Proyek

Dalam era digital yang terus berkembang, *MobilePhones* telah menjadi perangkat yang tak terpisahkan dari kehidupan sehari-hari masyarakat. Data dari berbagai sumber menunjukkan bahwa *MobilePhones* telah menjadi salah satu barang esensial dengan tingkat penetrasi yang sangat tinggi di kalangan penduduk Indonesia. Hal ini mengindikasikan bahwa permintaan terhadap *MobilePhones* semakin meningkat.

Dalam industri *MobilePhones*, harga menjadi salah satu faktor kunci yang mempengaruhi keputusan pembelian konsumen. Oleh karena itu, kemampuan untuk memprediksi harga *MobilePhones* secara akurat menjadi sangat penting bagi produsen, penjual, dan konsumen yang ingin membeli *MobilePhones* sesuai dengan anggaran dan kebutuhan mereka.

Pendekatan Machine Learning dengan teknik Clustering dapat menjadi solusi yang efektif dalam melakukan analisis harga *MobilePhones*. Dengan mengelompokkan *MobilePhones* berdasarkan fitur-fitur tertentu, seperti ukuran baterai dan harga terbaik, kita dapat memahami pola-pola harga yang ada dan membuat prediksi harga untuk *MobilePhones* baru berdasarkan kelompok-kelompok yang telah terbentuk.

Pada proyek ini, akan dilakukan analisis harga *MobilePhones* menggunakan teknik Clustering dari data *phones_data*. Sebagai langkah awal, data akan disiapkan dan dibersihkan untuk memastikan kualitas data yang baik. Selanjutnya, fitur-fitur yang relevan akan dipilih dan dilakukan scaling data untuk memastikan keseragaman skala pada fitur-fitur tersebut.

Metode Clustering yang akan digunakan, seperti K-Means Clustering, Agglomerative Clustering, DBSCAN Clustering, dan Mean Shift Clustering, akan membantu kita mengelompokkan *MobilePhones* berdasarkan fitur-fiturnya. Evaluasi akan dilakukan dengan menggunakan metrik Silhouette Score untuk mengukur kualitas klustering yang dihasilkan oleh setiap metode.

Dengan demikian, proyek ini bertujuan untuk memberikan wawasan yang lebih mendalam tentang pola harga *MobilePhones* berdasarkan fitur-fiturnya dan memberikan prediksi harga untuk *MobilePhones* baru dengan pendekatan Clustering yang dapat membantu industri *MobilePhones* dalam mengambil keputusan bisnis yang lebih tepat.

 

## Business Understanding



Pada era digital saat ini, *MobilePhones* menjadi perangkat yang sangat penting dan banyak diminati oleh masyarakat. Setiap tahun, banyak varian *MobilePhones* baru dengan beragam fitur dan spesifikasi yang diluncurkan oleh berbagai produsen. Hal ini menyebabkan variasi harga *MobilePhones* menjadi sangat bervariasi, tergantung pada fitur-fitur yang ditawarkan.

Masalah yang dihadapi adalah banyaknya variasi fitur dan harga *MobilePhones* yang ada membuat calon pembeli seringkali bingung dalam memilih *MobilePhones* yang sesuai dengan kebutuhan dan anggaran mereka. Kebutuhan akan model *machine learning* yang dapat memberikan prediksi harga *MobilePhones* dengan akurat menjadi semakin penting untuk membantu calon pembeli dalam mengambil keputusan yang tepat.

Tujuan dari proyek ini adalah untuk mengembangkan model *machine learning* menggunakan teknik Clustering yang dapat memprediksi harga *MobilePhones* berdasarkan fitur-fitur yang dimiliki. Dengan menggunakan data *phones_data* yang mencakup informasi mengenai fitur-fitur *MobilePhones* seperti ukuran baterai, harga terbaik, ukuran layar, dan lainnya, kita akan mencoba mengelompokkan *MobilePhones* ke dalam kelompok-kelompok yang memiliki kemiripan fitur dan kemudian memprediksi harga untuk *MobilePhones* baru berdasarkan kelompok-kelompok tersebut.

 

### Problem Statements

Berdasarkan permasalahan yang telah dijelaskan, *problem statements* dari proyek ini adalah sebagai berikut.

1. Bagaimana melakukan pengelompokkan (*clustering*) *MobilePhones* berdasarkan fitur-fiturnya, seperti harga terbaik dan kapasitas baterai?
2. Apa saja kelompok (*cluster*) yang terbentuk dari proses *clustering* tersebut?
3. Bagaimana kita dapat memahami perbedaan karakteristik dan pola harga *MobilePhones* di setiap kelompok (*cluster*) yang terbentuk?
4. Dapatkah kita menggunakan hasil *clustering* untuk memprediksi harga *MobilePhones* baru berdasarkan fitur-fitur yang dimiliki?

 

#### Goals

Tujuan yang hendak dicapai dari proyek ini adalah sebagai berikut

1. Mengelompokkan *MobilePhones* menjadi beberapa kelompok (*cluster*) berdasarkan fitur-fiturnya, untuk memahami pola dan karakteristik harga yang ada.
2. Menemukan pola harga dan karakteristik *MobilePhones* yang berbeda di setiap kelompok (*cluster*) yang terbentuk.
3. Memberikan wawasan dan rekomendasi berdasarkan analisis hasil *clustering* untuk membantu keputusan bisnis dalam penentuan harga dan strategi pemasaran *MobilePhones*.
4. Menerapkan hasil *clustering* sebagai langkah awal dalam membangun model prediksi harga *MobilePhones* baru berdasarkan fitur-fitur tertentu.

Dengan mencapai tujuan di atas, diharapkan proyek ini dapat memberikan manfaat dan pemahaman lebih dalam tentang pola harga *MobilePhones* berdasarkan fitur-fiturnya, serta memberikan panduan bagi industri *MobilePhones* dalam mengoptimalkan strategi bisnis dan pemasaran produk.

 

#### Solution Statements

Solusi yang diajukan untuk menyelesaikan masalah yang telah diuraikan adalah sebagai berikut.

1. Melakukan analisis eksplorasi data untuk memahami pola dan hubungan antara fitur-fitur yang mempengaruhi harga *MobilePhones*.
2. Menggunakan teknik *clustering* untuk mengelompokkan data *MobilePhones* berdasarkan kesamaan fitur-fiturnya.
3. Melakukan visualisasi hasil *clustering* untuk memahami karakteristik dan perbedaan antara kelompok-kelompok *MobilePhones* yang terbentuk.
4. Melakukan evaluasi kualitas *clustering* menggunakan metrik *silhouette score* untuk menentukan seberapa baik kelompok-kelompok tersebut terbentuk.
5. Memilih model *clustering* dengan *silhouette score* tertinggi sebagai model yang paling baik dalam mempartisi data *MobilePhones*.

 

## Data Understanding 

Dataset yang digunakan pada proyek ini diperoleh dari Kaggle. Silahkan kunjungi tautan berikut [Mobile Phones Data]( https://www.kaggle.com/datasets/artempozdniakov/ukrainian-market-mobile-phones-data) untuk mengakses dataset yang dipakai. Adapun variabel-variabel yang terdapat pada dataset adalah sebagai berikut :

 

1. **brand_name**: Nama merek telepon (String)
2. **model_name**: Nama model telepon (String)
3. **os**: Sistem operasi telepon (String)
4. **popularity**: Tingkat popularitas telepon (Integer)
5. **best_price**: Harga terbaik telepon (Float)
6. **lowest_price**: Harga terendah telepon (Float)
7. **highest_price**: Harga tertinggi telepon (Float)
8. **sellers_amount**: Jumlah penjual (Integer)
9. **screen_size**: Ukuran layar telepon (Float)
10. **memory_size**: Ukuran memory telepon (Float)
11. **battery_size**: Ukuran baterai telepon (Float)
12. **release_date**: Tanggal rilis telepon (String)

 

Ringkasan statistik dari data-data numerikal

![numeric](D:\RANGGA P\@@KULIAH RANGGA\@KULIAH2023_SMSTR4\AI\TUBES\phone\numeric.png)

 

## Data Preparation

Teknik data preparation yang dilakukan pada proyek ini adalah sebagai berikut:

1. Mengisi Missing Values: Melakukan pengisian nilai yang kosong (missing values) pada dataset. Jika terdapat kolom-kolom yang memiliki missing values, dapat menggunakan metode seperti pengisian nilai median atau mean dari kolom tersebut.

   ![missing values](D:\RANGGA P\@@KULIAH RANGGA\@KULIAH2023_SMSTR4\AI\TUBES\phone\missing values.jpeg)

2. Menghilangkan/ memeriksa Duplikasi Data: Memeriksa dan menghapus data yang memiliki duplikasi untuk mencegah pengaruh data duplikat pada analisis.

![duplicate](D:\RANGGA P\@@KULIAH RANGGA\@KULIAH2023_SMSTR4\AI\TUBES\phone\duplicate.jpeg)



3. Pemilihan Fitur: Memilih fitur atau variabel yang relevan untuk dilibatkan dalam analisis. Dalam proyek ini, kita akan menggunakan fitur seperti 'best_price', 'battery_size', dan lainnya yang relevan untuk prediksi harga *MobilePhones*.



![pilih_fitur](D:\RANGGA P\@@KULIAH RANGGA\@KULIAH2023_SMSTR4\AI\TUBES\phone\pilih_fitur.jpeg)



4. Scaling Data: Melakukan penskalaan pada data numerik jika diperlukan, terutama jika skala nilai antar fitur berbeda jauh. Scaling data dapat dilakukan dengan menggunakan metode seperti StandardScaler atau MinMaxScaler.

![scalling](D:\RANGGA P\@@KULIAH RANGGA\@KULIAH2023_SMSTR4\AI\TUBES\phone\scalling.jpeg)



5. Encoding Data Kategorikal: Jika terdapat fitur-fitur kategorikal, perlu dilakukan encoding untuk mengubahnya menjadi bentuk numerik agar dapat digunakan dalam analisis. Contohnya, kita dapat menggunakan metode Label Encoding atau One-Hot Encoding.

6. Visualisasi Data: Melakukan visualisasi data untuk melihat persebaran data dan hubungan antar fitur. Visualisasi data dapat membantu dalam pemahaman pola-pola yang ada dalam data.



![visualisas_data](D:\RANGGA P\@@KULIAH RANGGA\@KULIAH2023_SMSTR4\AI\TUBES\phone\visualisas_data.jpeg)



Seluruh teknik data preparation di atas dilakukan untuk memastikan data yang digunakan dalam analisis memiliki kualitas yang baik, sehingga model machine learning yang dihasilkan dapat memberikan prediksi yang akurat untuk harga *MobilePhones*.

 

Pada tahap Modeling, kita akan membuat model machine learning menggunakan teknik clustering untuk menyelesaikan permasalahan prediksi harga MobilePhones. Berikut adalah tahapan dan parameter yang digunakan pada proses pemodelan:

1. **Pemilihan Fitur**: Sebelum melakukan clustering, kita perlu memilih fitur-fitur yang akan digunakan sebagai input dalam proses clustering. Pada contoh kode sebelumnya, kita memilih fitur 'best_price' dan 'battery_size' sebagai fitur yang akan digunakan dalam teknik clustering.

 

![pilih_fitur](D:\RANGGA P\@@KULIAH RANGGA\@KULIAH2023_SMSTR4\AI\TUBES\phone\pilih_fitur.jpeg)

 

2. **Scaling Data**: Sebelum melakukan clustering, kita perlu melakukan scaling data pada fitur-fitur yang dipilih. Scaling data dilakukan untuk mengubah skala data agar memiliki mean 0 dan standard deviation 1, sehingga memudahkan proses clustering.

 

![scalling](D:\RANGGA P\@@KULIAH RANGGA\@KULIAH2023_SMSTR4\AI\TUBES\phone\scalling.jpeg)

 

3. **Pilihan Metode Clustering**: Pada contoh kode sebelumnya, kita menggunakan beberapa metode clustering, yaitu K-Means Clustering, Agglomerative Clustering, DBSCAN Clustering, dan Mean Shift Clustering.

 ![metodeclustering](D:\RANGGA P\@@KULIAH RANGGA\@KULIAH2023_SMSTR4\AI\TUBES\phone\metodeclustering.jpeg)

 

4. **Parameter Metode Clustering**: Setiap metode clustering memiliki parameter yang perlu ditentukan sebelum proses clustering dilakukan. Pada contoh kode sebelumnya, menggunakan beberapa parameter seperti jumlah kluster (n_clusters) pada K-Means Clustering, eps dan min_samples pada DBSCAN Clustering, dan sebagainya. Nilai-nilai parameter ini dapat diubah-ubah untuk mencari hasil clustering yang optimal.

5. **Melakukan Clustering**: Setelah fitur-fitur dan parameter telah ditentukan, kita dapat melakukan proses clustering menggunakan metode-metode yang telah dipilih dengan memanggil fungsi fit_predict() dari masing-masing model clustering.

![fitpredict](D:\RANGGA P\@@KULIAH RANGGA\@KULIAH2023_SMSTR4\AI\TUBES\phone\fitpredict.jpeg)



6. **Visualisasi Hasil Clustering**: Setelah clustering selesai, kita dapat melakukan visualisasi hasil clustering untuk melihat pola dan kelompok yang terbentuk pada data. Pada contoh kode sebelumnya, kita menggunakan scatter plot untuk memvisualisasikan hasil clustering dengan warna yang berbeda untuk setiap kelompok.

 ![code clustering](D:\RANGGA P\@@KULIAH RANGGA\@KULIAH2023_SMSTR4\AI\TUBES\phone\code clustering.jpeg)



**hasil**

![outputhasil](D:\RANGGA P\@@KULIAH RANGGA\@KULIAH2023_SMSTR4\AI\TUBES\phone\outputhasil.png)

 

Selain tahapan di atas, dalam pemodelan dengan teknik clustering, kita juga dapat melakukan evaluasi clustering dengan menggunakan metrik seperti Silhouette Score, untuk mengevaluasi seberapa baik clustering yang dihasilkan.



![evaluasi](D:\RANGGA P\@@KULIAH RANGGA\@KULIAH2023_SMSTR4\AI\TUBES\phone\evaluasi.jpeg)



**Tahapan dan Parameter Pemodelan**

1. K-Means Clustering:

·     Algoritma: K-Means

·     Jumlah Cluster (K): 3 (parameter yang dapat diatur)

·     Random State: 42 (parameter untuk inisialisasi random seed)

2. Agglomerative Clustering:

·     Algoritma: Agglomerative Clustering

·     Jumlah Cluster (K): 3 (parameter yang dapat diatur)

3. DBSCAN Clustering:

·     Algoritma: DBSCAN

·     Epsilon (eps): 0.5 (parameter yang dapat diatur)

·     Min Samples: 5 (parameter yang dapat diatur)

4. Mean Shift Clustering:

·     Algoritma: Mean Shift

·     Bandwidth: Tidak ada parameter bandwidth yang ditentukan secara eksplisit, karena dalam contoh kode yang diberikan, kita menggunakan parameter bandwidth yang diestimasi secara otomatis oleh algoritma.

Kelebihan dan Kekurangan Algoritma Clustering yang Digunakan

1. K-Means Clustering:

·     Kelebihan:

o  Sederhana dan mudah diimplementasikan.

o  Cepat dalam eksekusi untuk jumlah data yang besar.

·     Kekurangan:

o  Harus menentukan jumlah cluster (K) terlebih dahulu.

o  Rentan terhadap inisialisasi cluster yang acak, sehingga hasil clustering bisa berbeda-beda.

 

2. Agglomerative Clustering:

 

·     Kelebihan:

o  Tidak perlu menentukan jumlah cluster sebelumnya.

o  Hasil clustering berbentuk dendrogram yang bisa membantu memilih jumlah cluster yang sesuai.

·     Kekurangan:

o  Lebih lambat dalam eksekusi dibandingkan dengan K-Means.

 

3. DBSCAN Clustering:

·     Kelebihan:

o  Tidak perlu menentukan jumlah cluster sebelumnya.

o  Bisa mengidentifikasi noise dan menggabungkan cluster berbentuk tidak teratur (non-spherical).

·     Kekurangan:

o  Parameter epsilon dan min samples harus dipilih secara hati-hati agar mendapatkan hasil clustering yang baik.

 

4. Mean Shift Clustering:

·     Kelebihan:

o  Tidak perlu menentukan jumlah cluster sebelumnya.

o  Cocok untuk data dengan bentuk cluster yang tidak teratur dan memiliki banyak noise.

·     Kekurangan:

o  Memiliki kompleksitas komputasi yang tinggi, terutama untuk jumlah data yang besar.

 

**Pemilihan Model Terbaik dan Improvement**

Karena menggunakan beberapa algoritma clustering, akan memilih model terbaik berdasarkan hasil evaluasi performa clustering dengan menggunakan Silhouette Score. Silhouette Score mengukur seberapa baik setiap data berada dalam cluster yang sama dibandingkan dengan cluster lainnya. Semakin mendekati nilai 1, semakin baik clusteringnya.

Berdasarkan prinsip bahwa semakin mendekati nilai 1, semakin baik clusteringnya, maka dapat disimpulkan bahwa DBSCAN dan Mean Shift adalah model terbaik untuk menyelesaikan permasalahan prediksi harga MobilePhones dalam proyek ini. Kedua algoritma ini memiliki performa clustering yang lebih baik dibandingkan dengan K-Means dan Agglomerative Clustering.

 

Dalam proyek ini, menggunakan metrik evaluasi Silhouette Score untuk mengevaluasi hasil dari teknik clustering yang digunakan (K-Means, Agglomerative Clustering, DBSCAN, dan Mean Shift). Metrik Silhouette Score digunakan untuk mengukur sejauh mana objek dalam sebuah cluster similar satu sama lain dan berbeda dari cluster lainnya. Nilai Silhouette Score berkisar dari -1 hingga 1, di mana nilai yang lebih tinggi menunjukkan clustering yang lebih baik.

Hasil dari evaluasi proyek ini berdasarkan metrik Silhouette Score adalah sebagai berikut:

\- K-Means Clustering: Silhouette Score = 0.4401

\- Agglomerative Clustering: Silhouette Score = 0.4407

\- DBSCAN Clustering: Silhouette Score = 0.6121

\- Mean Shift Clustering: Silhouette Score = 0.6012

Dari hasil evaluasi di atas, dapat disimpulkan bahwa DBSCAN memiliki nilai Silhouette Score tertinggi, diikuti oleh Mean Shift, K-Means, dan Agglomerative Clustering. Ini menunjukkan bahwa DBSCAN dan Mean Shift memberikan hasil clustering yang lebih baik dibandingkan dengan K-Means dan Agglomerative Clustering.

Bahwa metrik evaluasi hanyalah satu aspek dalam mengevaluasi model clustering. Selain Silhouette Score, kita juga perlu mempertimbangkan interpretasi hasil clustering dan kesesuaian dengan tujuan proyek. Selain itu, dalam kasus ini, kami juga menggunakan teknik visualisasi untuk membantu memahami hasil clustering dengan lebih baik.

Dengan demikian, hasil proyek ini menunjukkan bahwa DBSCAN dan Mean Shift adalah teknik clustering yang lebih baik dalam memprediksi harga MobilePhones berdasarkan fitur-fitur tertentu yang digunakan dalam dataset phones_data.

berikut adalah penjelasan lebih rinci tentang metrik evaluasi yang digunakan dalam proyek ini, yaitu Silhouette Score:

#### Silhouette Score

Silhouette Score adalah metrik evaluasi yang digunakan untuk mengukur sejauh mana objek dalam sebuah cluster similar satu sama lain dan berbeda dari cluster lainnya. Metrik ini memberikan nilai antara -1 hingga 1, di mana:

\- Nilai negatif dekat dengan -1 menunjukkan bahwa objek lebih cocok untuk dikelompokkan dalam cluster lain.

\- Nilai dekat dengan 0 menunjukkan bahwa objek berada di dekat batas antara dua cluster, dan dapat berarti ada ketidakjelasan dalam pembagian kluster.

\- Nilai dekat dengan 1 menunjukkan bahwa objek sangat cocok untuk dikelompokkan dalam clusternya.

Formula Silhouette Score untuk setiap objek i dalam dataset adalah:

Silhouette Score(i) = (b(i) - a(i)) / max(a(i), b(i))

Di mana:

\- a(i) adalah rata-rata jarak objek i ke semua objek lain dalam kluster yang sama dengan i (pembagian dalam-cluster).

\- b(i) adalah jarak rata-rata objek i ke semua objek dalam kluster yang berbeda dengan i (pembagian antar-cluster).

Untuk menghitung Silhouette Score keseluruhan dari suatu clustering, kita mengambil rata-rata Silhouette Score dari semua objek dalam dataset.

Semakin tinggi nilai Silhouette Score, semakin baik kualitas clusteringnya, karena menunjukkan bahwa objek dalam sebuah cluster lebih mirip satu sama lain dan lebih berbeda dari cluster lainnya.

Dalam proyek ini, menggunakan metrik Silhouette Score untuk mengevaluasi performa dari berbagai teknik clustering yang digunakan (K-Means, Agglomerative Clustering, DBSCAN, dan Mean Shift) dalam memprediksi harga MobilePhones berdasarkan fitur-fitur tertentu yang ada dalam dataset phones_data.

 

## Conclussion

1. Dalam proyek ini, menggunakan teknik clustering untuk memprediksi harga MobilePhones berdasarkan fitur-fitur tertentu yang ada dalam dataset phones_data. Tujuan dari proyek ini adalah untuk mengetahui fitur-fitur yang paling berkorelasi dengan penentuan harga MobilePhones, membuat model machine learning yang dapat memprediksi harga MobilePhones, dan memilih model dengan akurasi terbaik berdasarkan proses preprocessing yang dilakukan.

2. Kami mulai dengan melakukan analisis deskriptif terhadap data untuk mengetahui pola dan informasi yang tersimpan di dalamnya. Setelah itu, kami melakukan data manipulation untuk menggabungkan kolom-kolom yang berpengaruh terhadap akurasi prediksi harga MobilePhones. Kemudian, kami melakukan preprocessing dengan mengecek missing value dan duplikasi data, menghapus kolom yang tidak berpengaruh, melakukan visualisasi data untuk melihat persebaran dan korelasi antar kolom, serta melakukan encoding terhadap kolom kategorikal.

3. Setelah proses data preparation, kami melakukan teknik clustering menggunakan beberapa algoritma, yaitu K-Means, Agglomerative Clustering, DBSCAN, dan Mean Shift. Evaluasi clustering dilakukan dengan menggunakan metrik Silhouette Score, yang mengukur sejauh mana objek dalam sebuah cluster similar satu sama lain dan berbeda dari cluster lainnya. Dari hasil evaluasi, diperoleh bahwa model dengan menggunakan algoritma DBSCAN memiliki nilai Silhouette Score tertinggi, yaitu 0.6121, yang menunjukkan kualitas clustering yang lebih baik dibandingkan dengan algoritma lainnya.

Dengan demikian, proyek ini memberikan wawasan tentang penggunaan teknik clustering dalam memprediksi harga MobilePhones dan dapat digunakan sebagai dasar untuk penelitian lebih lanjut dalam bidang ini.

 

## Referensi

[1] Lutfia Afifah, "Apa itu Regresi, Klasifikasi, dan Clustering (Klasterisasi)?" 2023 [online]. Available: (https://ilmudatapy.com/apa-itu-regresi-klasifikasi-dan-clustering-klasterisasi/)

[2] Baiam Uma, "Jenis-jenis metode dalam clustering" 2021 [online]. Available: (https://bamai.uma.ac.id/2021/12/23/jenis-jenis-metode-dalam-clustering/)



**---Ini adalah bagian akhir laporan---**
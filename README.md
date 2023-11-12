
# Data Storytelling :  Steakhouse Jakarta 2022

Steakhouse merupakan salah satu jenis restoran yang populer di Jakarta, menawarkan berbagai varian daging sapi yang lezat dan berbagai macam hidangan kuliner yang menggugah selera. Namun, masih ada konsumen yang bingung untuk memilih steakhouse yang tepat untuk dinikmati. Untuk menambah preferensi konsumen dan memperbaiki layanan pemilik steakhouse yang belum berhasil, diperlukan analisis data steakhouse yang ada di Jakarta berdasarkan rating dan harga rata-rata menu menggunakan SMART Questions.

## SMART Question

|Specific|Measureable|Action-oriented|Relevant|Time-Bound|
|:----:|:----:|:----:|:----:|:----:|
|“Steakhouse mana saja yang memiliki rating paling rendah?” “Berapa rata-rata rating dari restoran steakhouse di Jakarta?” “Berapa rentang harga makanan steak di restoran-restoran tersebut?”|“Bagaimana korelasi antara rating restoran dan harga makanannya?” “Berapa banyak restoran yang memiliki rating diatas 4.0?”|“Bisakah kita mengidentifikasi restoran steakhouse terbaik di Jakarta?” “Hal apa yang perlu dilakukan pemilik restoran untuk meningkatkan rating steakhouse tersebut?”| “Apakah aksi tersebut dapat meningkatkan rating steakhouse? ”| “Berapa lama rencana peningkatan tersebut dilaksanakan?”|

Dari perntanyaan di atas diharapkan mampu menggiring data menghasilkan sebuah jawaban yang meaningful insights.

## Data Wrangling
Setelah mendeskripsikan latar belakang dan merumuskan pertanyaan untuk analisis ini, tahap berikutnya adalah data wrangling. Analisis pada tahap ini dibagi menjadi tiga proses, yaitu mengumpulkan data, menyiapkan data untuk dianalisis, dan membersihkan data.

### 1. Mengumpulkan Data
Langkah pertama yang perlu dilakukan pada tahap ini adalah menyiapkan dataset yang diperlukan untuk analisis, yaitu dataset “Steakhouse Jakarta 2022” seperti yang tertera pada gambar di bawah ini.

![Screenshot 2023-11-10 212930](https://github.com/redshoes11/DataStorytelling_SteakhouseJakarta2022/assets/80873008/013bba10-88ef-4d7d-9f58-4c1fbb3e605a)

Data diambil dari Kaggle : https://www.kaggle.com/datasets/miradelimanr/steakhouse-jakarta/data yang dikompilasi dari Google Maps, Zomato, dan PergiKuliner dan sudah diperbaharui 1 Agustus 2022.
### 2. Menyiapkan Data untuk Dianalisis
Setelah melakukan pengumpulan data, proses selanjutnya adalah menyiapkan data. Langkah ini dilakukan untuk menilai kualitas dan struktur dari sebuah data. Selain itu, proses ini juga bertujuan untuk mengidentifikasi berbagai masalah yang terdapat dalam data, seperti missing value, understand values, dll.
Hanya saja pada dataset tersebut masih terdapat inconsistent data serta kolom yang tidak diperlukan pada proses analisis ini sehingga perlu dibersihkan agar proses analisis data tidak terdistraksi oleh data-data yang tidak perlu.

### 3. Membersihkan Data
Pada proses pembersihan data, dilakukan proses penghapusan kolom-kolom yang tidak diperlukan untuk mempermudah proses analisis data. Selain itu, dilakukan penghapusan untuk data yang duplikat, missing values, dan data-data yang tidak masuk akal.
Setelah pembersihan data, tersisa 178 data yang dapat dianalisis dari 187 data. Sehingga, tampilan data akan seperti gambar di bawah.

![image](https://github.com/redshoes11/DataStorytelling_SteakhouseJakarta2022/assets/80873008/51636d4d-f236-4266-bac2-fd727a1af3d9)

Dari data yang sudah dibersihkan didapatkan nilai : 
1. Rata-rata Google Rating = 4
2. Rata-rata Platform Rating = 3,787078652
3. Range Harga Steak = Rp 242.608,-

![image](https://github.com/redshoes11/DataStorytelling_SteakhouseJakarta2022/assets/80873008/c52e75e6-7ab7-460b-ba90-8c7b3f896dee)


## Eksplorasi Data (Exploratory Data Analysis)

Tahap ini merupakan proses mengidentifikasi hubungan (korelasi) dan tren dalam data untuk dapat menjawab SMART Questions.
Dalam tahap eksplorasi data terdapat 4 tahap yang perlu dilalui, yaitu : 

### 1. Mengatur Data
Tahap ini sudah dilewati saat proses data wrangling sebelumnya. Data diatur mulai dari menyiapkan, mengumpulkan, dan membersihkan data.

### 2. Memformat dan menyesuaikan data.
Pada tahap ini dilakukan format tipe data untuk setiap kolom. Pada kolom google_rating dan platform_rating bertipe data float. Pada kolom price, google_count, dan platform_count bertipe data integer. Pada kolom restaurant_name, city dan specialized bertipe data string.

### 3. Mendapatkan insights dari orang lain.
Selain menganalisis berdasarkan data, proses eksplorasi data ini diambil dari beberapa sumber mulai dari wawancara warga setempat terkait faktor yang menyebabkan ada beberapa restoran steakhouse mendapatkan rating rendah, dll.

### 4. Amati hubungan antar titik data dan membuat perhitungan.
Pada tahap ini dilakukan perhitungan nilai korelasi untuk mencari hubungan antara dua variabel. 

**_1. Google Rating - Google Review (Count)_**

Data X = Google Rating
Data Y = Google Review (Count)

Nilai Korelasi = 0,200470461

![image](https://github.com/redshoes11/DataStorytelling_SteakhouseJakarta2022/assets/80873008/337a0822-4629-4b39-8925-a92c59c5f623)

Dari nilai korelasi tersebut dapat disimpulkan bahwa korelasi antara Google Rating dan Google Reviews memiliki hubungan karena memiliki nilai korelasi positif hanya saja tidak memiliki hubungan yang kuat karena masih jauh dari angka 1.
Setelah mengetahui korelasi tersebut, tahap selanjutnya adalah mencari tren dari data di atas maka langkah selanjutnya adalah perlu menggunakan grafik yang tepat, yaitu scatter plot.

![image](https://github.com/redshoes11/DataStorytelling_SteakhouseJakarta2022/assets/80873008/7327176f-d367-4392-8f25-61fc7ab0eade)

Dari nilai korelasi yang telah didapatkan yaitu 0.2 dan grafik scatter tidak menunjukan tren yang signifikan, maka dapat disimpulkan bahwa antara **Goggle Rating dan Google Review tidak memiliki hubungan atau korelasi yang kuat** satu sama lain.

**_2. Platform Rating - Platform Review (Count)_**

Data X = Platform Rating
Data Y = Platform Review (Count)

Nilai Korelasi = 0,487921942

![image](https://github.com/redshoes11/DataStorytelling_SteakhouseJakarta2022/assets/80873008/7c17fe3a-502f-4252-bb48-3a00156cc775)

Dari nilai korelasi tersebut dapat disimpulkan bahwa korelasi antara Platform Rating dan Platform Reviews memiliki hubungan karena memiliki nilai korelasi positif hanya saja tidak memiliki hubungan yang kuat karena masih jauh dari angka 1.
Setelah mengetahui korelasi tersebut, tahap selanjutnya adalah mencari tren dari data di atas maka langkah selanjutnya adalah perlu menggunakan grafik yang tepat, yaitu scatter plot.

![image](https://github.com/redshoes11/DataStorytelling_SteakhouseJakarta2022/assets/80873008/9c19644c-f9f5-47dc-9fc8-2cb34f639586)

Dari nilai korelasi yang telah didapatkan yaitu 0.4 dan grafik scatter tidak menunjukan tren yang signifikan, maka dapat disimpulkan bahwa antara **Platform Rating dan Platform Review tidak memiliki hubungan atau korelasi yang kuat** satu sama lain.

**_3. Google Rating - Price_**

Data X = Google Rating
Data Y = Price 

Nilai Korelasi = 0,140203707

![image](https://github.com/redshoes11/DataStorytelling_SteakhouseJakarta2022/assets/80873008/0c032d45-379c-45d2-bca8-161792dd79e5)

Dari nilai korelasi tersebut dapat disimpulkan bahwa korelasi antara Google Rating dan Price memiliki hubungan karena memiliki nilai korelasi positif hanya saja tidak memiliki hubungan yang kuat karena masih jauh dari angka 1.
Setelah mengetahui korelasi tersebut, tahap selanjutnya adalah mencari tren dari data di atas maka langkah selanjutnya adalah perlu menggunakan grafik yang tepat, yaitu scatter plot.

![image](https://github.com/redshoes11/DataStorytelling_SteakhouseJakarta2022/assets/80873008/6517d977-6057-4c63-b1f4-e79a4b6774cd)

Dari nilai korelasi yang telah didapatkan yaitu 0.1 dan grafik scatter tidak menunjukan tren yang signifikan, maka dapat disimpulkan bahwa antara **Goggle Rating dan Price tidak memiliki hubungan atau korelasi yang kuat** satu sama lain.


**_4. Platform Rating - Price_**

Data X = Platform Rating
Data Y = Price 

Nilai Korelasi = 0,077320189

![image](https://github.com/redshoes11/DataStorytelling_SteakhouseJakarta2022/assets/80873008/3cfd327c-a804-4661-96c6-121b751a955c)

Dari nilai korelasi tersebut dapat disimpulkan bahwa korelasi antara Platform Rating dan Price memiliki hubungan karena memiliki nilai korelasi positif hanya saja tidak memiliki hubungan yang kuat karena masih jauh dari angka 1.
Setelah mengetahui korelasi tersebut, tahap selanjutnya adalah mencari tren dari data di atas maka langkah selanjutnya adalah perlu menggunakan grafik yang tepat, yaitu scatter plot.

![image](https://github.com/redshoes11/DataStorytelling_SteakhouseJakarta2022/assets/80873008/838306dd-622d-4489-8479-2b06fa322be5)

Dari nilai korelasi yang telah didapatkan yaitu 0.07 dan grafik scatter tidak menunjukan tren yang signifikan, maka dapat disimpulkan bahwa antara **Platform Rating dan Price tidak memiliki hubungan atau korelasi yang kuat** satu sama lain.

## Data Visualization
Setelah melakukan berbagai langkah dalam menganalisis data, tahap ini merupakan memvisualisasikan data yang ada pada dataset tersebut.
* Jumlah Google Rating Steakhouse di Jakarta per-kategori.
  ![image](https://github.com/redshoes11/DataStorytelling_SteakhouseJakarta2022/assets/80873008/f2c3a911-a628-4dfb-b9c1-9076473f7e4c)

* Jumlah Platform Rating Steakhouse di Jakarta per-kategori.
  ![image](https://github.com/redshoes11/DataStorytelling_SteakhouseJakarta2022/assets/80873008/a96b6fc0-b538-4f5b-9192-228ffddeaef3)

## Kesimpulan
Maka dari itu setelah dilakukan analisis diatas, dapat disimpulkan bahwa ada 17 restoran yang berada dibawah rata-rata untuk Google rating dan ada 61 restoran yang berada dibawah rata-rata untuk Platform rating. Rata-rata rating dari restoran steakhouse di Jakarta berdasarkan Google rating dan Platform rating adalah 4 dan 3,7. Rentang harga makanan steak di restoran-restoran tersebut adalah Rp242.608,-. Restoran Tucano's Churrascaria merupakan restoran yang mendapat rating bagus baik dari google Rating dan Platform Rating. Dari berbagai macam restoran-restoran tersebut, restoran yang perlu diperhatikan Parkiran Steak & Bar dan Roellie’s karena memiliki rating rendah di kedua data baik Google Rating dan Platform Rating. Sehingga, hal yang dapat dilakukan untuk meningkatkan rating steakhouse tersebut adalah dengan mulai untuk mempromosikan lebih luas lagi. Upaya ini akan dilakukan uji coba dalam rentang waktu satu kuartal atau sekitar empat bulan mulai dari Januari hingga April. Setelah dilakukan uji tersebut maka perlu analisis kembali terkait upaya meningkatkan destinasi tersebut.







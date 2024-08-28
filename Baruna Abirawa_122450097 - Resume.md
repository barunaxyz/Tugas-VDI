Nama : Baruna Abirawa

NIM : 122450097

Kelas : RA

# Visualisasi Data dan Informasi
------------------------------

## Pendahuluan

Visualisasi data adalah data abstrak yang diubah menjadi bentuk, warna, dan sebagainya yang secara langsung akan menyajikan data tersebut secara visual. Dengan visualisasi data kita dapat dengan mudah menyimpulkan hasil analisis dari suatu data. 

![image](https://github.com/user-attachments/assets/de794a5f-096f-4659-a030-7620396a692d)

Terdapat suatu grafik berulang yang dimana diawali oleh Data Import, Data Preparation, Data Manipulation, Mapping, dan Rendering.
  1. Data Import untuk mengambil data yang diperlukan dari sumber data yang diinginkan.
  2. Data preparation adalah mempersiapkan data yang diimpor untuk visualisasi, misalnya dengan menormalkan nilai, mengoreksi entri yang salah, dan menginterpolasi nilai yang hilang.
  3. Data Manipulation adalah memilih data yang akan divisualisasikan (pemfilteran dari komunitas visualisasi) dan mungkin dengan operasi umum lainnya seperti penggabungan dan pengelompokan.
  4. Mapping adalah memetakan data yang diperoleh dari proses di atas ke bentuk yang geometris (misalnya titik dan garis). beserta atributnya (misalnya warna, posisi, dan ukuran).
  5. Rendering adalah mengubah data geometris di atas menjadi representasi visual.

Berdasarkan dari grafik berulang, ada 3 cara untuk membuat visualisasi data lebih efisien dan lebih efektif yaitu terdiri dari Spesifikasi Visualisasi, Pendekatan Efisien untuk Visualisasi data, dan Rekomendasi Visualisasi data.
  1. Spesifikasi Visualisasi
       - Kelengkapan diri : Penting bagi pembaca untuk mengetahui cara menghasilkan visualisasi data.
       - Perspektif desain bahasa : Menentukan cara memetakan informasi yang berbeda ke elemen visual
  2. Pendekatan Efisien untuk Visualisasi Data
     Agar dapat meilbatkan pengguna secara efektif dalam alur berulang, proses pembuatan visualisasi data harus efisien dan terukur, terutama untuk dua komponen yaitu *Data Manipulation* dan *Mapping*.
  3. Rekomendasi Visualisasi Data
     Untuk menentukan visualisasi secara tepat sulit dilakukan, bahkan bagi para ahli, hanya karena pemahamannya tentang data apa yang akan divisualisasikan, cerita mana yang harus diceritakan, dan bagaimana memvisualisasikan. Oleh karena itu, penting agar sistem visualisasi dapat memandu pengguna secara cerdas dengan memberikan rekomendasi.

## Spesifikasi Visualisasi

Spesifikasi terbagi menjadi tiga bagian penting yaitu Data, Marks, dan Mapping. Data adalah data yang perlu divisualisasikan, tanda adalah representasi visual seperti batang, garis, atau titik. Sedangkan mapping adalah memetakan data ke tanda yang sesuai.

Terdapat 4 kategori dalam bahasa visualisasi data sebagai berikut.

![image](https://github.com/user-attachments/assets/717ddf48-4a48-411b-8bf9-82cf61167328)

1. Low level languages adalah bahasa tingkat rendah sebagai bahasa yang pengguna perlukan untuk menentukan semua elemen pemetaan.
2. High level languages bahasa tingkat tinggi merangkum detail konstruksi visualisasi, seperti fungsi pemetaan, serta beberapa properti untuk tanda seperti ukuran kanvas, legenda, dan properti lainnya.
3. GUI Based Tools dibandingkan dengan menggunakan bahasa visualisasi deklaratif untuk menentukan visualisasi seperti yang dibahas sebelumnya, cara yang lebih mudah digunakan dalam memberikan spesifikasi adalah dengan mengikuti "prinsip manipulasi langsung". Terdapat daftar alat berbasis GUI yang canggih yaitu Tableau, Qlik, Excel, Google Sheets, dan sebagainya.
4. Underspecified Language visualisasi tidak ada artinya jika tidak dapat memberikan gambaran tentang data. Namun dalam banyak kasus, pengguna tidak benar benar mengetahui semua aspek data yang ada, karena datanya mungkin besar dan datanya sering diperbarui. Oleh karena itu, hal ini menimbulkan persyaratan untuk mendukung spesifikasi yang tidak ditentukan.

## Efficient approaches for data visualization

Visualisasi data yang tepat yaitu menghitung visualisasi yang tepat secepat mungkin. Namun terkadang, memberikan visualisasi yang tepat tidak selalu dapat dilakukan karena esarnya ukuran data dan tingginya kompleksitas kueri. Maka dari itu, ada beberapa cara untuk membuat visualisasi yang efisien.

- Query Translation cara alami untuk menggunakan kembali banyak sistem yang sudah matang (DBMS) adalah dengan menerjemahkan kueri visualisasi ke kueri yang diterima sistem tersebut.
  ![image](https://github.com/user-attachments/assets/4675bddc-c7e5-4fff-8315-ba03e27d1d94)
- Integrating Visualization systems with DBMS ada beberapa kelemahan yaitu salah satunya masalah utama adalah banyaknya fungsi yang diulang. Sehingga menghasilkan teknik optimasi yang tidak terpadu dengan asumsi dan kinerja yang berbeda di server dan klien sehingga membuat pengembang bingung untuk memilih optimasi yang sesuai.
- Column store dalam pengelolaan data, faktor kinerja utama adalah tata letak data, misalnya tata letak berbasis baris dan berbasis kolom, yang mungkin memiliki perbedaan kinerja yang besar untuk aplikasi OLAP. Dalam hal visualisasi data, pengguna biasanya hanya tertarik pada beberapa kolom. Tentu saja, penyimpanan kolom dapat mencapai kinerja yang lebih baik, dibandingkan dengan penyimpanan baris, yang telah diadopsi di SeeDB.
- Indexes banyak digunakan untuk meningkatkan kinerja pencarian dengan mengurangi jumlah record/baris dalam tabel yang perlu diperiksa. Tentu saja, mereka memainkan peran penting dalam meningkatkan kinerja visualisasi data
- Parallel Computation komputasi paralel juga telah banyak digunakan untuk pemrosesan kueri dalam sistem visualisasi data. Harald dkk menyediakan arsitektur multithreading untuk eksplorasi visualisasi interaktif.
- Prediction and Prefetching salah satu langkah penting dalam visualisasi data adalah eksplorasi data, pengguna terus menelusuri visualisasi yang mereka minati untuk mendapatkan gambaran tentang apa yang akan divisualisasikan. Seringkali visualisasi yang dieksplorasi saat ini biasanya terinspirasi dari visualisasi sebelumnya. Dengan kata lain, pengguna bisa mendapatkan informasi detail/keseluruhan, dan lain-lain.

## Visualization Recommendation

Visualisasi data bersifat berulang, dan masalah utama para praktisi adalah mereka harus terlibat dalam setiap langkah untuk membuat beberapa modifikasi. Tentu saja, sangat diharapkan adanya beberapa solusi rekomendasi visualisasi yang membuat hidup pengguna lebih mudah, dengan merekomendasikan visualisasi yang baik kepada mereka. Berikut ini adalah cara memilih visualisasi yang cocok pada suatu permasalahan:
- Pruning Meaningless Visualizations yaitu memangkas visualisasi yang tidak berarti dan dapat digunakan untuk memangkas visualisasi yang "buruk".
- User-specified constraints pengguna dapat menentukan elemen visualisasi yang diminati seperti kolom atau rekaman data.
- Expert provided constraints beberapa kombinasi variabel, transformasi, dan pengkodean visual mungkin tidak menghasilkan visualisasi yang valid. Misalnya, tipe tanda "pie" tidak dapat digabungkan dengan tipe pengkodean "tinggi", dan tipe pengkodean "sumbu Y" tidak cocok untuk atribut kategorikal.

## Other research directions
- ### Data preparation for data visualization
Data di kehidupan nyata biasanya kotor, dan memvisualisasikan data kotor dapat menyesatkan pengguna. Fenomena ini sudah dikenal sejak lama sebagai salah satu jenis visualisasi bias dari komunitas visualisasi data. Misalnya, kumpulan data yang terintegrasi dari berbagai sumber mungkin berisi duplikat. Secara alami, data yang divisualisasikan harus dibersihkan,seperti normalisasi nilai, deduplikasi, imputasi nilai yang hilang, dan deteksi outlier. Tableau telah mengintegrasikan Trifacta untuk persiapan data di seluruh kumpulan data.

- ### Data visualization benchmarks
Sangat penting untuk mengembangkan tolok ukur kinerja dan rekomendasi. Tolok ukur tersebut harus sesuai dengan tugas analisis visual, memberikan jejak dan data yang dapat digunakan kembali, dan jika ada rekomendasi, memiliki cakupan dan kualitas label yang tinggi. Terdapat fokus yang muncul pada pengembangan tolok ukur yang muncul pada pengembangan tolok ukur untuk ukuran kinerja.

- ### Data visualization for database-related applications
  - Excel
  - Google Sheets
  - Oracle Data Visualization Dekstop
  - IBM Db2
  - Amazon Quicksight
  - Microsoft Power BI

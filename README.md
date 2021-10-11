# Laporan Proyek Machine Learning - Zulfazazalia Putri Candra Wati

## Domain Proyek
Jual beli mobil bekas telah berlangsung cukup lama dan menjadikan ceruk bisnis tersendiri. Bahkan banyak sekali showroom mobil bekas yang menawarkan harga dan kualitas yang sepadan. Namun, bagi masyarakat yang ingin menjual mobil bekas harus memperhatikan dan mempertimbangkan berapa harga pasaran mobil yang sesuai dengan harga pasar yang ada Karena tidak mungkin ketika ingin menjual mobil kita memberikan harga yang sama seperti saat kita membeli mobil baru. Kualitas produk mobil bekas pun juga mempengaruhi keputusan konsumen untuk membeli. Karena kualitas mobil bekas menjadi tolak ukur konsumen dalam menilai kelayakan mobil untuk dibeli.

Salah satu mobil bekas yang akan dibahas saat ini adalah “VW” atau bisa disebut “Volkswagen”. Menurut [Wikipedia](https://id.wikipedia.org/wiki/Volkswagen), "Volkswagen" sendiri memiliki arti dalam bahasa jerman yaitu "mobil rakyat". Volkswagen sendiri merupakan pabrik otomotif berbasis di Wolfsburg, Lower Saxony, Jerman. Dari artikel [idntimes](https://www.idntimes.com/automotive/car/meiska-irena-pramudhita-1/5-hal-ini-bikin-vw-klasik-masih-banyak-diburu-bisa-buat-investasi/5) alasan seseorang menyukai mobil VW salah satunya adalah desain yang ikonik serta bisa menjadi investasi. Dari penjelasan diatas, membuat saya memilih menggunakan dataset penjualan mobil bekas “VW” untuk proyek ini. 

Pada dataset ini terdiri dari informasi harga, transmisi, jarak tempuh, jenis bahan bakar, pajak jalan, mil per galon (mpg), dan ukuran mesin, model mobil, dan tahun pendaftaran. Serta dalam proyek ini memiliki tujuan untuk memprediksi harga jual dari mobil bekas dengan merek VW. Dengan predictive analytic diharapkan dapat memprediksi solusi dari permasalahan ini.

## Business Understanding
Bagi seseorang yang ingin menjual mobilnya perlu mengetahui harga pasar dari mobil tersebut. Oleh karena itu perlu adanya sistem dalam memprediksi harga jual mobil bekas VW dengan teknik predictive modelling. Semisal, saat menjual mobil kita memasang harga yang sama dengan harga jual mobil dengan kualitas mobil yang tidak sama dengan mobil baru maka pelanggan yang ingin membeli mobil bekas tidak mengambil mobil yang kita jual dan lebih memilih mobil bekas dengan harga murah dan kualitas mobilnya yang lumayan bagus. Dari kasus ini yang menyebabkan penjual mobil bekas memerlukan sistem untuk memprediksi harga.

### Problem Statements 
Dari kondisi diatas, maka kita dapat membuat prediksi harga jual mobil sebagai berikut:
* Fitur apakah yang dapat berpengaruh dalam memprediksi harga jual mobil bekas VW?
* Berdasarkan fitur yang ada, model apakah yang tepat dalam memprediksi harga jual mobil bekas VW?

### Goals 
Dari pernyaatan masalah diatas maka kita dapat membuat tujuan atau goals seperti berikut:
* Mengetahui fitur yang cocok atau berpengaruh dalam memprediksi harga jual mobil bekas VW
* Mengetahui model yang tepat dalam memprediksi harga jual mobil VW berdasarkan fitur yang ada

### Solution Statements 
Saat memprediksi harga jual mobil, saya menggunakan model regresi dan price sebagai target. Dalam penyelesaian masalah ini, saya menggunakan 3 solusi model algoritma machine learning yang memiliki penjelasan sebagai berikut:
* <b>Decision Tree</b> : Model ini merupakan salah satu algoritma supervised learning yang dapat dipakai untuk masalah klasifikasi dan     regresi.Decision tree juga merupakan komponen pembangun utama algoritma Random Forest. Pada model ini, memiliki   kelebihan yaitu dibuat secara numerik atau kategorik dan memerlukan sedikit pemrosesan data di awal pembuatan.
* <b>Random Forest</b> : Pada algoritma ini disusun dari banyak decision tree yang pembagian data dan fiturnya dipilih secara acak.Penggunaan random forest mampu mengklasifiksi data yang memiliki atribut yang tidak lengkap dan dapat digunakan untuk menangani data sampel yang banyak. 
* <b>AdaBoost (Boosting)</b> : AdaBoost atau Adaptive Boost merupakan algoritma ensemble yang memanfaatkan bagging dan boosting untuk mengembangkan peningkatan akurasi. Cara kerja dari AdaBoost sendiri yaitu pada awal suatu kasus memiliki data latih dengan weight atau bobot yang sama. Bobot yang lebih tinggi kemudian diberikan pada model yang salah sehingga mereka akan dimasukkan ke dalam tahapan selanjutnya. Proses iteratif ini berlanjut sampai model mencapai akurasi yang diinginkan. Kelebihan dari model ini yaitu relatif lebih mudah untuk diimplementasikan dan waktu pengujian yang relatif cepat sehingga cocok dipakai dalam implementasi kondisi real time.

## Data Understanding
Pada proyek ini saya menggunakan dataset yang tersedia pada Kaggle. Dataset ini memiliki 15.157 jenis mobil merek VW dengan beberapa fitur baik fitur numerik dan kategorikal. Penggunaan metrik pada prediksi ini menggunakan *Mean Squared Error* (MSE). Untuk variable yang ada pada dataset [100,000 UK Used Car Data set](https://www.kaggle.com/adityadesai13/used-car-dataset-ford-and-mercedes) adalah sebagai berikut:
*	model: merupakan model dari mobil VW dan masuk pada fitur kategorikal, dari yang paling banyak yaitu model “Golf” dan paling sedikit yaitu model “Eos”.
*	year : merupakan tahun dari registrasi dan masuk pada fitur numerik (2000-2020)
*	price: merupakan harga dalam euro (£) dan menjadi fitur target dalam prediksi ini
*	transmission : merupakan tipe dari gearbox dan masuk pada fitur kategorikal (Manual,Semi-Auto, dan Automatic)
*	mileage : merupakan jarak yang di tempuh dan masuk pada fitur numerik
*	fuelType : merupakan jenis bahan bakar mesin dan masuk pada fitur kategorikal (Petrol, Diesel, Hybrid, Other)
*	tax : merupakan pajak jalan dan masuk pada fitur numerik (0-580)
*	mpg : merupakan mil per gallon dan masuk pada fitur numerik (0.3-188)
*	engineSize : merupakan ukuran mesin dan masuk pada fitur numerik (0-3.2)

Untuk proyek ini saya terdapat tahapan salah satunya yaitu teknik visualisasi data. Penjelasan serta visualisasi data akan dibahas sebagai berikut:

Pada tahapan data understanding terdapat penanganan outliers dimana pada saat mengecek outliers menggunakan teknik visualisasi data dengan menggunakan boxplot. Visualisasi data outliers dilakukan pada fitur numerik. Pada fitur numerik terdiri dari year, price, mileage, mpg, engineSize, dan tax.
![outliers1 jpg](https://user-images.githubusercontent.com/81318203/136737513-793341f2-5fee-4a78-a88b-c91e465bfd44.png)
![outliers3](https://user-images.githubusercontent.com/81318203/136737737-79f44601-c400-4535-aa13-799908f382ed.png)

Kemudian pada analisis univariate dan multivariate terdapat visualisasi data yang berasal dari numerical dan kategorikal. Untuk fitur kategori yang pertama dari analisis univariate (Univariate EDA) yaitu “model” dimana pada fitur ini menampilkan model dari mobil VW.
![model1 jpg](https://user-images.githubusercontent.com/81318203/136737933-b6a62b49-d04c-4aea-b32f-fae627165214.png)
![model2](https://user-images.githubusercontent.com/81318203/136740919-8c8813b6-d165-47bb-b045-707124300415.jpg)
Bila dilihat dari grafik terdapat 25 kategori model mobil VW. Bila kita urutkan fitur model dari jumlah terbanyak ke terkecil yaitu Golf, Polo, Tiguan, Up, Passat, T-Roc, Touran, T-Cross, Sharan, Arteon, Golf SV, Scirocco, Touareg, Amarok, Tiguan Allspace, CC, Betle, Shuttle, Caddy Maxi Life, Jetta, Caravelle, Caddy Life, Caddy, Caddy Maxi, Eof. Pada jumlah sampel untuk model yang memiliki jumlah terbanyak adalah Golf sedangkan untuk model “Eos” memiliki jumlah data paling sedikit. Dan bila dilihat dari persentase maka lebih dari 60% model yang masuk pada grade tinggi yaitu Golf, Polo, Tiguan.

Selanjutnya untuk fitur kedua yaitu transmission akan menampilkan tipe dari gearbox. 
![trans1](https://user-images.githubusercontent.com/81318203/136741051-b76b9312-bb2e-4055-a5cc-1b6c1e7736c3.jpg)
![trans2](https://user-images.githubusercontent.com/81318203/136741059-7db5b374-59c1-481b-b662-02b4f3c05868.jpg)
Pada fitur ini memiliki 3 kategori yang terdiri dari tipe manual, semiauto dan automatic. Bila dilihat dari persentase, data “Manual” memiliki persentase terbanyak yaitu 62% sedangkan “Semi-Auto” memiliki persentase terbanyak kedua yaitu 25 % dan persentase terkecil berada pada “Automatic”. Sehingga untuk transmission yang memiliki grade tertinggi yaitu Manual.

Dan untuk fitur yang terakhir yaitu fuel type dimana pada data ini menampilkan jenis bahan bakar.
![type1](https://user-images.githubusercontent.com/81318203/136741942-60a7d96f-f33b-434a-9211-b6e4ddefed8a.jpg)
![type2](https://user-images.githubusercontent.com/81318203/136741946-ec4b6d09-c671-4567-ac09-64914187121c.jpg)
Terdapat 4 kategori pada fitur fuel type yaitu diesel, hybrid, petrol dan other. Bila dilihat dari jumlah sampel maka penggunaan jenis bahan bakar terbanyak ke terendah memiliki uruatan sebagai berikut yaitu petrol, diesel, other dan hybrid. Saat dilihat dari persentase maka 60% grade tertinggi dari jenis bahan bakar ada pada petrol.

![kategori1](https://user-images.githubusercontent.com/81318203/136742517-3920474a-ef98-4559-bedf-51276ac2a822.jpg)
![kategori2](https://user-images.githubusercontent.com/81318203/136742522-80586916-3e21-4d65-9975-6ff34b53c80e.jpg)
Pada visualisasi diatas merupakan 3 gambar yang menampilkan perbandingan rata-rata price terhadap fitur kategori dari anlisis multivariate (Multivariate EDA) seperti rata-rata price dengan model, rata-rata price dengan transmission, dan rata-rata price dengan fuel type. Visualisasi data ini membuat saya menemukan beberapa informasi yaitu baik pada fitur model, transmission, fuel type hasil dari grafiknya berkebalikan dengan grafik pada analisis univariate yang dimaksud dari penjelasan ini bila kita lihat di grafik diatas ini pada fitur model yang tertinggi yaitu “Caravelle” sedangkan pada grafik sebelumnya grade tertinggi berada pada grafik model “Golf”, selain itu juga bila kita lihat pada fitur fuel type dimana semakin rendah grade jenis bahan bakar maka harganya semakin tinggi dan yang terakhir pada fitur transmission yang sebelumnya automatic terendah menjadi tertinggi dan manual menjadi yang terendah. Dari sini dapar disimpulkan bahwa fitur kategori memiliki dampak yang rendah terhadap harga.

Kemudian pada analisis univariate dari fitur numerik dapat dilihat pada gambar histogram dibawah ini terdapat year, price sebagai target, mileage, tax, mpg dan engineSize. Bila dilihat dari histogram “price” yang menjadi target pada data ini bahwa pada grafik rentang 10.000-15.000(£) memiliki harga terbanyak bila dibandingkan dengan rentang harga lainnya. Dari data tersebut dapat dilihat bahwa bila ingin melakukan penjualan mobil dapat memberikan harga dari rentang tersebut. Harga tersebut dapat menarik perhatiaan seseorang bila ingin membeli mobil bekas tersebut.
![numerik1](https://user-images.githubusercontent.com/81318203/136742614-8d1fc0a1-6710-4f3d-bebb-29eb8fec857a.jpg)

Selanjutnya bila kita analisis dengan teknik Multivariate EDA dari fitur numerik dapat kita amati hubungan antar fitur numerik dengan menggunakan fungsi pairplot. Dari gambar dibawah ini bila kita liat dari pola sebaran grafik terlihat year, mileage, dan mpg memiliki korelasi tinggi dengan “price” sedangkan tax dan engineSize memiliki korelasi yang lemah karena tidak adanya bentuk pola sebaran. Oleh karena itu, untuk memastikan korelasi yang didapat tadi benar maka dapat mengeceknya dengan menggunakan fungsi corr().
![numerik2](https://user-images.githubusercontent.com/81318203/136742696-1d8fd5d9-6f40-4935-a926-8c5ee6b990aa.jpg)

Bila kita lihat pada gambar dibawah ini kita dapat mengamati korelasi matrik untuk fiur numerik yang didapat. Dimana fitur year, mileage, tax dan mpg memiliki nilai korelasi yang besar dengan fitur price seperti year mendapat skor 1, price mendapat skor 0.62, mileage -0.77, tax mendapat skor 0.52, mpg mendapat skor 0.48. Dari sini terlihat bahwa keempat fitur itu memiliki korelasi tinggi dengan price. Sedangkan pada fitur engineSize memiliki korelasi yang kecil dimana nilainya mendekati nilai 0 yaitu 0.01. Oleh karena itu untuk fitur engineSize di drop karena memiliki korelasi yang lemah.
![korelasi1](https://user-images.githubusercontent.com/81318203/136742764-0f5ad501-c872-40df-b354-8204c9b98516.jpg)

## Data Preparation

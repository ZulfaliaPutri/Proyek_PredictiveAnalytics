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
* <b>AdaBoost</b> : AdaBoost atau Adaptive Boost merupakan algoritma ensemble yang memanfaatkan bagging dan boosting untuk mengembangkan peningkatan akurasi. Cara kerja dari AdaBoost sendiri yaitu pada awal suatu kasus memiliki data latih dengan weight atau bobot yang sama. Bobot yang lebih tinggi kemudian diberikan pada model yang salah sehingga mereka akan dimasukkan ke dalam tahapan selanjutnya. Proses iteratif ini berlanjut sampai model mencapai akurasi yang diinginkan. Kelebihan dari model ini yaitu relatif lebih mudah untuk diimplementasikan dan waktu pengujian yang relatif cepat sehingga cocok dipakai dalam implementasi kondisi real time.




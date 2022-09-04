# **ECOMMERCE CUSTOMER CHURN PREDICTION AND ANALYSIS**

A final project assigned by Purwadhika Digital Technological School completed by 2 members of group: 
- Kenshi Poneva Yulindo
- Luthfi Ghina Barka

# **BUSINESS PROBLEM**

## *1.1 Context*

Pada dasarnya, customer churn terjadi ketika pelanggan yang berhenti menggunakan produk atau layanan dari suatu bisnis di perusahaan. Perpindahan atau kehilangan pelanggan adalah salah satu masalah paling krusial bagi bisnis apapun yang secara langsung menjual atau melayani pelanggan, salah satunya adalah bisnis e-commerce.

Di kasus ini, sebuah perusahaan e-commerce memiliki masalah churn dimana 16,8% pelanggannya melakukan churn pada periode terakhir. Dengan alasan ini, e-commerce bersangkutan telah mengontrak kami dalam sebuah proyek untuk membangun model prediktif yang akurat. 

Oleh karena itu, tugas kami sebagai data scientist adalah mengidentifikasi masalah, menganalisa data untuk mendapatkan insights, membuat model machine learning dengan algoritma yang mampu memprediksi seakurat mungkin pada pelanggan yang churn dan tidak, dan memberikan rekomendasi berdasarkan hasil yang kita dapat secara keseluruhan.

Berikut adalah definisi masing-masing label pada e-commerce ini:  
 
    0 = Pelanggan yang tidak churn (loyal customer)  
    Pelanggan yang tidak churn di perusahaan ini ditandai dengan angka yang cenderung tinggi pada hari terakhir mereka bertransaksi, jumlah order, serta lama berlangganan. 
    
    1 = Pelanggan yang churn (berhenti/pindah) 
    Pelanggan yang tidak churn di perusahaan ini ditandai dengan angka yang cenderung rendah pada hari terakhir mereka bertransaksi, jumlah order, serta jenis barang yang dibeli (pembelian barang elektronik yang cenderung churn). 

## *1.2 Problem Understanding*

Faktanya, persentase pelanggan yang hilang tersebut berpengaruh terhadap growth rate perusahaan, ini merupakan alasan utama yang menjadikan customer churn rate begitu penting terutama di bisnis e-commerce. 

Selain itu, sebuah survey membuktikan bahwa:
- mendapatkan pelanggan baru bisa menghabiskan biaya sekitar 5x lipat dibandingkan jika kita memelihara hubungan pelanggan yang sudah ada. 
- Tingkat keberhasilan (success rate) pada penjualan ke pelanggan yang sudah ada adalah 60-70%, sedangkan tingkat keberhasilan penjualan ke pelanggan baru adalah 5-20%. 
- Meningkatkan tingkat retensi pelanggan sebesar 5% meningkatkan keuntungan sebesar 25-95%.

Dengan alasan ini, dibandingkan jika kita melakukan customer acquisition, memperhatikan dan meningkatkan hubungan dengan pelanggan yang sudah ada akan memberikan keuntungan jangka panjang pada perusahaan seperti peningkatan customer life value dan pengaruhnya terhadap profit perusahaan. Namun tantangannya adalah, jika kita tidak tahu pelanggan manakah yang akan churn maka kita akan cenderung menargetkan semua pelanggan dimana ini dapat menyia-nyiakan biaya retention cost. 

## *1.3 Problem Statement*

Setelah memahami latar belakang permasalahan, kita mampu menyimpulkan problem statement pada projek ini. Ada 2 poin penting yang menjadi landasan kita yaitu Goals dan Values. Goals kita disini sesuai konteks yang sudah dijelaskan di awal yaitu untuk memprediksi customer churn seakurat mungkin dengan tujuan utama kita yaitu untuk meminimalkan biaya retention cost dan juga meningkatkan customer life value.

Disini kita akan melakukan prediksi menggunakan machine learning dengan metode Supervised Learning (Binary Classification). Selain memberikan prediksi pada customer churn, pihak manajemen juga berharap bisa mengetahui faktor/variabel yang mempengaruhi seorang pelanggan yang churn atau tidak, sehingga mereka dapat membuat strategi yang baik dalam mengurangi tingkat churn yang tinggi.

## *1.4 Metric Analysis*

Jadi, model yang kita cari adalah model yang memberikan prediksi akurat pada kelas positif dengan nilai recall setinggi mungkin untuk menghindari kehilangan pelanggan berpotensi loyal diikuti dengan nilai Precision yang juga harus sama tingginya untuk menghindari terbuangnya biaya yang dialokasikan. Jadi kita harus menyeimbangkan antara precision dan recall dari 1 kelas positive. Maka metric utama yang akan kita gunakan adalah **f1-score** namun tetap memperhatikan nilai **recall** agar lebih tinggi dari **precision**. Selain itu, tujuan menggunakan f1-score adalah salah satu metode untuk mengatasi ketidakseimbangan data pada kelas positif (churn) dan kelas negatif (not churn).

# **ECOMMERCE CUSTOMER CHURN PREDICTION AND ANALYSIS**

A final project assigned by Purwadhika Digital Technological School completed by 2 members of group: 
- Kenshi Poneva Yulindo
- Luthfi Ghina Barka

# **BUSINESS PROBLEM**

## *1.1 Context*

Customer churn adalah metrik bisnis yang mengukur jumlah pelanggan yang telah berhenti menggunakan produk atau layanan dari suatu bisnis di perusahaan. Perpindahan atau kehilangan pelanggan adalah salah satu masalah paling krusial bagi bisnis apapun yang secara langsung menjual atau melayani pelanggan, salah satunya adalah bisnis e-commerce.

Di kasus ini kami diberikan tanggung jawab untuk menangani prediksi customer churn pada bisnis e-commerce di bidang retail.   
Jadi, pihak manajemen ingin mengetahui pelanggan mana yang cenderung memiliki persentase tinggi untuk berhenti melakukan pembelian/berpindah ke e-commerce lain. Hal ini bertujuan untuk mengurangi kerugian perusahaan yang disebabkan pada pelanggan yang hilang. 

Maka dari itu, divisi Data Science bertanggung jawab untuk mengidentifikasi peluang yang dihasilkan dari data yang tersedia. Dalam kasus ini, kita sebagai anggota tim Data Scientist ditugaskan untuk dapat memprediksi calon pelanggan mana saja yang akan churn dan diminta untuk membuat model Machine Learning yang akan digunakan oleh Tim Marketing dari e-commerce bersangkutan.

## *1.2 Problem Statement*

Faktanya, persentase pelanggan yang hilang tersebut berpengaruh terhadap growth rate perusahaan, ini merupakan alasan utama yang menjadikan customer churn rate begitu penting terutama di bisnis e-commerce. 

Selain itu, sebuah survey membuktikan bahwa:
- mendapatkan pelanggan baru bisa menghabiskan biaya sekitar 5x lipat dibandingkan jika kita memelihara hubungan pelanggan yang sudah ada. 
- Tingkat keberhasilan (success rate) pada penjualan ke pelanggan yang sudah ada adalah 60-70%, sedangkan tingkat keberhasilan penjualan ke pelanggan baru adalah 5-20%. 
- Meningkatkan tingkat retensi pelanggan sebesar 5% meningkatkan keuntungan sebesar 25-95%.

Dengan alasan ini, memperhatikan dan meningkatkan hubungan dengan pelanggan yang sudah ada akan lebih hemat biaya dan lebih menghasilkan profit dibandingkan jika kita melakukan customer acquisition. 


## *1.3 Goals*

Berdasarkan permasalahan tersebut, pihak manajemen ingin memiliki kemampuan untuk melakukan prediksi seakurat mungkin atas pelanggan yang akan churn. Ini dapat membantu mereka dalam membuat keputusan untuk mengantisipasi situasi tersebut. Maka dari itu, kita akan melakukan prediksi menggunakan machine learning dengan metode Supervised Learning (Classification).

Selain memberikan prediksi pada customer churn, pihak manajemen juga berharap bisa mengetahui faktor/variabel yang mempengaruhi seorang pelanggan yang churn atau tidak, sehingga mereka dapat membuat strategi yang baik dalam mengurangi tingkat churn yang tinggi.

## *1.4 Metric Analysis*

Mengacu pada *metric evaluation* diatas, kita perlu meminimalisir bagian False Negative Rate (meminimalkan profit loss) yang juga berarti memaksimalkan True Positive Rate (memaksimalkan profit perusahaan). Jadi, model yang diinginkan adalah model yang mampu mengurangi resiko kehilangan customer yang berpotensial tanpa membuang waktu dan biaya pemasaran pada customer yang sudah loyal. Jadi kita harus menyeimbangkan antara precision dan recallnya dari 1 kelas positive. Maka metric utama yang akan kita gunakan adalah **f1-score**.

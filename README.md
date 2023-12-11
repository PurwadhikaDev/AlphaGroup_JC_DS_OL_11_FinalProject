# AlphaGroup_JC_DS_OL_11_FinalProject
This project was carried out by Alpha's Team:
1. Akmal Azaki
2. Ahmad Baihaqi
3. Athian Istafa Yahya

## **Business Problem Understanding**
#### **Context**
Olist merupakan salah satu perusahaan marketplace terbesar di Brazil yang bergerak di segmen e-Commerce. Olist menghubungkan penjual e-commerce dengan customers secara mudah menggunakan single contract. Dengan demikian, para penjual dapat menjual produk mereka dan mengirimkan produk tersebut kepada customer melalui Olist logistics partners.
Setelah customer membeli produk melalui Olist store, para penjual mendapatkan notifikasi untuk memenuhi pesanan tersebut. Setelah customer menerima produk atau estimasi pengiriman sudah tersedia, customer mendapatkan survey kepuasan dimana para customers dapat memberikan review baik secara tulisan dan juga rating.
Sebagai data scientist, dataset yang tersedia pada Olist dapat dianalisa untuk mengetahui permasalahan yang sedang dihadapi Olist. Menurut ([Statista, 2023](https://www.statista.com/topics/4697/e-commerce-in-brazil/#topicOverview)), segmen e-commerce menghasilkan national total revenue sebesar 170 billion Brazilian reals di tahun 2022, meningkat 2 kali lipat dibandingkan 2019 dan naik sebesar 12% dari tahun 2021. Olist dapat memanfaatkan dataset yang dimiliki. Sehingga, analisis data tersebut menghasilkan kesimpulan dan rekomendasi yang terukur. Hal ini menjadi penting untuk dilakukan bagi Olist untuk mengambil kesempatan pada market yang berkembang pesat dan dapat memiliki competitive advantage diantara kompetitornya dengan cara meningkatkan performansi Olist.

#### **Problem Statement**
Berdasarkan Cohort analysis yang kita lakukan, terdapat suatu permasalahan dimana mayoritas setiap customer hanya melakukan frekuensi pembelian satu kali. Maka dari itu dibutuhkan solusi untuk meningkatkan frekuensi pembelian dalam E-commerce ini. Salah satu strategi yang dapat dilakukan yaitu melakukan Strategi pemasaran.
Aktivitas pemasaran dapat memakan waktu dan sumber daya yang berlebihan jika perusahaan tidak melakukan segmentasi pelanggan terlebih dahulu. Perusahaan ingin meningkatkan efektivitas dan efisiensi pemasaran dengan mengetahui pengelompokan dari setiap pelanggan sehingga perusahaan dapat memberikan metode pemasaran yang tepat untuk setiap pelanggannya.
Dan jika pemarasan yang diberikan tidak sesuai ataupun kurang optimal dengan jenis pelanggan, maka perusahaan beresiko kehilangan beberapa pelanggan, bahkan tidak dapat mengoptimalkan pelanggan potensial menjadi pelanggan tetap, dan tidak dapat mempertahankan pelanggan tetap.
Pada data e-commerce Olist, angka rata - rata cohort analisis dari customer Olist hanyalah sebesar 0.046%. Sehingga, Olist memiliki customer yang memiliki sifat engagement rendah terhadap pembelian pada Olist atau repeat order dari customer dapat dikatakan masih sangat rendah. Oleh karena itu, perlu dilakukan strategi marketing agar customer melakukan pembelian ulang pada Olist.
Namun, strategi marketing secara general untuk seluruh customer tidak akan efektif. Strategi marketing yang hendak dilakukan haruslah spesifik berdasarkan kebutuhan dan juga behaviour dari tiap customer Olist. Menurut [Temnjanovski dan Arsova, 2019](https://eprints.ugd.edu.mk/21568/), menyusun sebuah marketing strategi untuk segmentasi customer yang tepat penting untuk menghemat resources dan waktu. Oleh karena itu, terhadap data Olist, akan dilakukan segmentasi customer agar strategi marketing yang dilakukan sesuai dengan kebutuhkan tiap customer segment dari Olist.

#### **Goals**
Maka, berdasarkan probelm statement diatas. Goals dari project ini adalah sebagai berikut:
- Mengatahui customer behaviour seberapa sering customer melakukan pembelian di Olist melalui cohort analysis
- Melakukan cluster modelling untuk memprediksi segmentasi customer
- Memahami kebutuhan setiap customer segment dengan cara melakukan Exploratory Data Analysis terhadap hasil segmentasi
- Menentukan strategi marketing yang tepat untuk setiap segmentasi customer

#### **Analytic Approach**
Dalam project ini, kami menggunakan RFM Analysis dan K-Means Clustering dalam menentukan segmentasi pelanggan. RFM analysis membagi kebiasaaan pelanggan berdasarkan :
1. Recency: jumlah hari terakhir pelanggan melakukan transaksi
2. Frequency: frekuensi pembelian pelanggan
3. Monetary: nominal transaksi pelanggan

Untuk penentuan jumlah cluster menggunakan algoritma K-Means, kami menggunakan:
1. Silhouette Score: Silhouette Score mengukur seberapa baik setiap titik data ditempatkan dalam klasternya sendiri dibandingkan dengan klaster sekitarnya. Score ini berkisar antara -1 hingga 1, dan nilai yang lebih tinggi menunjukkan bahwa titik data tersebut ditempatkan dengan baik dalam klasternya dan berjauhan dari klaster lainnya. Jika Silhouette Score mendekati 1, itu menunjukkan bahwa klasternya sesuai.
Jika mendekati -1, itu menunjukkan bahwa titik data mungkin lebih baik ditempatkan dalam klaster lain. Nilai mendekati 0 menunjukkan tumpang tindih antar klaster.
2. Elbow Method berfokus pada varian intra-klaster sebagai fungsi dari jumlah klaster. Fungsi objektif yang diukur adalah jumlah kuadrat jarak antara setiap titik data dengan pusat klasternya. Jumlah klaster optimal dipilih di titik "siku" (elbow) di grafik, di mana penurunan varian mulai melambat.
3. Domain Knowledge untuk penyesuaian dan tujuan bisnis.

## **RFM Result**
![RFM](https://github.com/PurwadhikaDev/AlphaGroup_JC_DS_OL_11_FinalProject/blob/main/img/RFM%20Result.png)

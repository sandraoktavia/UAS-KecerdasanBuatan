# UAS-KecerdasanBuatan
1. Business Understanding
Masalah utama adalah penyebaran spam SMS yang merugikan. Sistem tradisional seperti pemblokiran kata kunci menjadi kurang efektif. Solusinya adalah menggunakan machine learning, khususnya algoritma K-Nearest Neighbors (KNN), untuk mendeteksi spam secara otomatis.
***
2. Tujuan Proyek
* Mengembangkan model klasifikasi SMS spam menggunakan KNN dan TF-IDF.
* Mengevaluasi kinerja model menggunakan akurasi, precision, recall, dan F1-score.
* Meminimalkan false positive dan false negative.
* Menyediakan baseline untuk sistem deteksi spam yang ringan.
---
3. Pengguna dan Manfaat
* Individu: Terhindar dari spam dan penipuan.
* Operator Seluler: Deteksi awal spam sebelum diteruskan ke pengguna.
* Bisnis Komersial: Menjamin pesan sah tidak terfilter.
* Developer Aplikasi: Dapat diintegrasikan ke dalam SMS gateway.
* Peneliti & Akademisi: Sebagai studi kasus baseline klasifikasi teks.
---
4. Data Understanding
* Dataset: SMS Spam Collection dari Kaggle, 5572 pesan (spam dan ham).
* Fitur: Teks pesan, panjang pesan, jumlah kata, huruf kapital, tanda seru.
* Format: CSV, terdiri dari kolom Category (label) dan Message.
---
5. Exploratory Data Analysis (EDA)
* Distribusi Kelas: Tidak seimbang (ham: 87.6%, spam: 12.4%).
* Feature Engineering: Tambahan fitur numerik dari teks.
* Korelasi: Panjang pesan dan huruf kapital berkorelasi positif dengan spam.
* Insight: Spam cenderung lebih panjang dan menekankan kata penting dengan huruf kapital & tanda seru.
---
6. Data Preparation
* Mengisi nilai kosong, label encoding pada target.
* Ekstraksi fitur teks menggunakan TF-IDF.
* Pembagian data: 80% train, 20% test dengan stratifikasi label.
---
7. Modeling
* Algoritma: K-Nearest Neighbors (KNN).
* Visualisasi: Scatter plot hasil PCA menunjukkan klasterisasi yang baik antara spam dan ham.
* KNN dipilih karena sederhana, non-parametrik, dan cocok sebagai baseline.
---
8. Evaluation dengan
 Confusion Matrix:
  * TN = 904
  * FP = 0
  * FN = 85
  * TP = 43
  * Akurasi: 91.8%
  * Precision (spam): 100%
  * Recall (pam): 33.6%
  * F1-score: 50.3%
  * Model sangat presisi tapi kurang sensitif terhadap spam.
---
9. Kesimpulan dan Rekomendasi
Proyek ini berhasil mengembangkan model klasifikasi spam SMS menggunakan algoritma K-Nearest Neighbors (KNN) dengan representasi fitur berbasis TF-IDF serta tambahan fitur numerik seperti panjang pesan, jumlah kata, rasio huruf kapital, dan jumlah tanda seru. Hasil evaluasi menunjukkan bahwa model memiliki akurasi yang tinggi sebesar 91.8% dan precision 100% untuk kelas spam, artinya seluruh prediksi spam benar adanya tanpa kesalahan klasifikasi pesan sah (ham). Namun demikian, nilai recall yang rendah (33.6%) menandakan bahwa sebagian besar pesan spam gagal dikenali oleh model, sehingga performa deteksi masih kurang optimal. Hal ini mengindikasikan bahwa meskipun model sangat hati-hati dalam menghindari false positive, ia masih belum cukup sensitif terhadap pesan spam. Oleh karena itu, disarankan agar penelitian selanjutnya menggunakan dataset yang lebih besar dan seimbang, menerapkan teknik balancing data seperti SMOTE, serta mengeksplorasi algoritma klasifikasi lain seperti Naive Bayes, SVM, atau Random Forest guna meningkatkan performa, terutama dalam mendeteksi kelas minoritas seperti spam.

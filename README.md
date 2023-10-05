# Laporan Proyek Machine Learning Heart-Attack-Prediction - Ega Fernanda Putra

## Domain Proyek

Penyakit jantung, khususnya serangan jantung, merupakan salah satu masalah kesehatan global yang serius. Menurut Organisasi Kesehatan Dunia (WHO), penyakit kardiovaskular adalah penyebab kematian nomor satu di dunia. Serangan jantung terjadi ketika aliran darah ke bagian otot jantung terhalang atau terputus, biasanya karena penyumbatan arteri koroner. Identifikasi faktor-faktor risiko yang berkontribusi terhadap serangan jantung sangat penting dalam upaya pencegahan dan penanganan penyakit ini.Proyek ini bertujuan untuk memprediksi risiko serangan jantung berdasarkan data kesehatan dan gaya hidup pasien. 

**Rubrik/Kriteria Tambahan (Opsional)**:
- Pencegahan: Mengidentifikasi individu yang berisiko tinggi serangan jantung dapat memungkinkan upaya pencegahan yang lebih efektif. Ini termasuk perubahan gaya hidup, pengawasan medis lebih ketat, dan penggunaan obat-obatan yang sesuai.
- Sumber Daya Kesehatan: Dalam sistem perawatan kesehatan yang terbatas, memprioritaskan pasien yang berisiko tinggi dapat membantu alokasi sumber daya medis dengan lebih efisien.

**Referensi**
- [World Health Organization (WHO) - Cardiovascular Diseases](https://www.who.int/health-topics/cardiovascular-diseases)

## Business Understanding

### Problem Statements

Menjelaskan pernyataan masalah latar belakang:
- Salah satu masalah yang dihadapi adalah ketidakpastian dalam menentukan faktor-faktor yang paling berkontribusi terhadap risiko serangan jantung. Beberapa faktor seperti riwayat keluarga, gaya hidup, dan aspek medis seringkali kompleks dan beragam. Ini menyulitkan dalam identifikasi yang cepat dan akurat terhadap individu yang berisiko tinggi serangan jantung.
- Meskipun ada pedoman umum untuk mengidentifikasi risiko serangan jantung, model prediktif yang lebih presisi masih dibutuhkan. Kehadiran faktor-faktor tertentu dapat memiliki dampak yang berbeda pada risiko serangan jantung pada individu tertentu

### Goals

Menjelaskan tujuan dari pernyataan masalah:
- Tujuan dari pernyataan masalah pertama adalah mengembangkan model prediksi risiko serangan jantung yang dapat mengidentifikasi individu yang berisiko tinggi berdasarkan beragam faktor kesehatan dan gaya hidup. Model ini akan membantu tenaga medis dan pasien dalam upaya pencegahan dan pengelolaan risiko serangan jantung.
- Tujuan dari pernyataan masalah kedua adalah meningkatkan akurasi model prediksi risiko serangan jantung dengan mempertimbangkan dampak faktor-faktor yang berbeda pada risiko individu. Ini akan memungkinkan kita untuk memberikan peringatan lebih dini dan solusi yang lebih tepat dalam pencegahan serangan jantung.

**Rubrik/Kriteria Tambahan (Opsional)**:

### Solution statements
- Akan digunakan dua algoritma berbeda untuk mencapai solusi. Pertama, **Logistic Regression** akan dipilih sebagai model baseline untuk melakukan klasifikasi risiko serangan jantung. Kemudian akan dicoba algoritma **Random Forest Classifier** sebagai model kedua. Disini akan dilakukan evaluasi kinerja model dan memilih yang memberikan hasil terbaik berdasarkan metrik evaluasi seperti akurasi, presisi, dan recall.
- Akan dilakukan eksplorasi model lain yang cocok untuk permasalahan ini, seperti **Decsion Tree**, **Gradient Boosting**, dan **K-Nearest Neighbors (KNN)**.Setelah itu akan dievaluasi kinerja semua model yang diusulkan dan memilih model yang paling sesuai.

## Data Understanding
Dataset ini menyediakan berbagai fitur yang komprehensif tentang kesehatan jantung dan pilihan gaya hidup, mencakup detail spesifik pasien seperti usia, jenis kelamin, kadar kolesterol, tekanan darah, denyut jantung, dan indikator seperti diabetes, riwayat keluarga, kebiasaan merokok, obesitas, dan konsumsi alkohol. Selain itu, faktor gaya hidup seperti jam olahraga, kebiasaan makan, tingkat stres, dan jam sedentari juga termasuk. Aspek medis yang mencakup masalah jantung sebelumnya, penggunaan obat-obatan, dan kadar trigliserida juga dipertimbangkan. Aspek sosioekonomi seperti pendapatan dan atribut geografis seperti negara, benua, dan belahan bumi juga dimasukkan. Dataset ini, yang terdiri dari 8763 catatan dari pasien di seluruh dunia, diakhiri dengan fitur klasifikasi biner penting yang menunjukkan adanya atau tidak adanya risiko serangan jantung, menyediakan sumber daya komprehensif untuk analisis prediktif dan penelitian kesehatan kardiovaskular.

Sumber Dataset:
- [Kaggle Heart Attack Risk Prediction Dataset](https://www.kaggle.com/datasets/iamsouravbanerjee/heart-attack-prediction-dataset/data).

### Variabel-variabel pada Kaggle Heart Attack Risk Prediction Dataset adalah sebagai berikut:
- Patient ID - Unique identifier for each patient
- Age - Age of the patient
- Sex - Gender of the patient (Male/Female)
- Cholesterol - Cholesterol levels of the patient
- Blood Pressure - Blood pressure of the patient (systolic/diastolic)
- Heart Rate - Heart rate of the patient
- Diabetes - Whether the patient has diabetes (Yes/No)
- Family History - Family history of heart-related problems (1: Yes, 0: No)
- Smoking - Smoking status of the patient (1: Smoker, 0: Non-smoker)
- Obesity - Obesity status of the patient (1: Obese, 0: Not obese)
- Alcohol Consumption - Level of alcohol consumption by the patient (None/Light/Moderate/Heavy)
- Exercise Hours Per Week - Number of exercise hours per week
- Diet - Dietary habits of the patient (Healthy/Average/Unhealthy)
- Previous Heart Problems - Previous heart problems of the patient (1: Yes, 0: No)
- Medication Use - Medication usage by the patient (1: Yes, 0: No)
- Stress Level - Stress level reported by the patient (1-10)
- Sedentary Hours Per Day - Hours of sedentary activity per day
- Income - Income level of the patient
- BMI - Body Mass Index (BMI) of the patient
- Triglycerides - Triglyceride levels of the patient
- Physical Activity Days Per Week - Days of physical activity per week
- Sleep Hours Per Day - Hours of sleep per day
- Country - Country of the patient
- Continent - Continent where the patient resides
- Hemisphere - Hemisphere where the patient resides
- Heart Attack Risk - Presence of heart attack risk (1: Yes, 0: No)

**Rubrik/Kriteria Tambahan (Opsional)**:
Berikut ini adalah Visualisasi yang dilakukan untuk mendapatkan insight dari data yang telah diperoleh

1. **Visualisasi Distribusi Jenis Kelamin (Sex)**:
   - Dilakukan visualisasi untuk mengetahui bagaimana data terdistribusi berdasarkan jenis kelamin, memberikan pemahaman awal tentang perbandingan antara pria dan wanita dalam dataset.

2. **Visualisasi Distribusi Usia (Age)**:
   - Dilakukan visualisasi distribusi usia pasien dalam dataset untuk memahami karakteristik umur pasien yang relevan dengan risiko serangan jantung.

3. **Visualisasi Kolesterol (Cholesterol)**:
   - Dilakukan visualisasi kolesterol untuk melihat sebaran nilai kolesterol dalam dataset, yang berkaitan dengan risiko serangan jantung.

4. **Visualisasi Heart Rate (Heart Rate)**:
   - Visualisasi ini memberikan pemahaman tentang sebaran denyut jantung pasien dalam dataset dan potensial korelasinya dengan risiko serangan jantung.

5. **Visualisasi Jam Tidur Per Hari (Sleep Hours Per Day) untuk Heart Attack Risk**:
   - Melalui visualisasi jam tidur per hari, data dijelaskan dalam konteks risiko serangan jantung untuk mengevaluasi dampak pola tidur terhadap risiko.

6. **Visualisasi Persentase Pasien Pengkonsumsi Alkohol, Perokok, Penderita Diabetes, Penderita Obesitas untuk Heart Attack**:
   - Dilakukan Visualisasi Persentase Pasien Pengkonsumsi Alkohol, Perokok, Penderita Diabetes, Penderita Obesitas dalam konteks risiko serangan jantung.

7. **Visualisasi Pendapatan (Income), BMI, Trigliserida, Tingkat Stres (Stress Level), Jumlah Hari Aktivitas Fisik (Physical Activity Days Per Week), Jam Tidur Per Hari (Sleep Hours Per Day), Jam Olahraga Per Minggu (Exercise Hours Per Week)**:
   - Melakukan visualisasi untuk fitur-fitur utama yang relevan dengan risiko serangan jantung, seperti pendapatan, BMI, trigliserida, tingkat stres, aktivitas fisik, dan pola tidur.
   - 
Berikut ini adalah hasil visualisasinya <br>
  <img src="Images/distribution.png" alt="dist" width="auto" height="auto">
  <img src="Images/distribution2.png" alt="dist2" width="auto" height="auto">
  <img src="Images/distribution3.png" alt="dist3" width="auto" height="auto">
  <img src="Images/sex.png" alt="gender" width="auto" height="auto">
  <img src="Images/viz.png" alt="viz" width="auto" height="auto"> <br>
  
Dengan melakukan eksplorasi data ini, tahap awal yang krusial telah diselesaikan untuk memahami karakteristik dataset dalam konteks risiko serangan jantung sebelum melangkah ke tahap pemodelan.
## Data Preparation
Dalam tahapan data preparation, telah dilakukan beberapa langkah penting untuk memastikan data  siap untuk pemodelan. Berikut adalah penjelasan tentang proses data preparation yang dilakukan beserta alasan mengapa setiap tahapan diperlukan:

1. **Mengecek Data Kosong**:
   - Proses: Memeriksa apakah ada nilai yang hilang atau kosong dalam dataset.
   - Alasan: Ini penting karena nilai yang hilang dapat memengaruhi kualitas dan hasil pemodelan. Langkah ini membantu Anda memastikan bahwa dataset tidak memiliki kekurangan data yang signifikan.

2. **Mengecek Duplikat Data**:
   - Proses: Memeriksa duplikat data dalam dataset.
   - Alasan: Duplikat data dapat mengganggu analisis dan pemodelan. Menghapus duplikat membantu memastikan setiap entri unik diwakili dengan benar.

3. **Mengecek Korelasi**:
   - Proses: Melakukan analisis korelasi antara fitur-fitur dalam dataset.
   - Alasan: Memahami korelasi antar fitur membantu Anda mengidentifikasi hubungan yang mungkin ada di antara mereka. Ini penting untuk memilih fitur yang relevan dalam pemodelan dan menghindari multicollinearity.

4. **Menghapus Kolom Tidak Diperlukan**:
   - Proses: Menghapus kolom yang dianggap tidak relevan atau tidak diperlukan untuk analisis risiko serangan jantung.
   - Alasan: Mengurangi jumlah fitur yang digunakan dalam pemodelan dapat meningkatkan efisiensi dan mencegah overfitting.

5. **Membuat Kategori Untuk Umur dan BMI**:
   - Proses: Membuat kategori untuk fitur "Age" (umur) dan "BMI" berdasarkan batasan tertentu.
   - Alasan: Kategorisasi fitur-fitur ini dapat membantu dalam memahami distribusi dan memungkinkan pemodelan yang lebih baik berdasarkan grup umur dan BMI.

6. **One-Hot Encoding dan Label Encoding**:
   - Proses: Menerapkan one-hot encoding dan label encoding pada fitur-fitur kategorikal.
   - Alasan: Model machine learning memerlukan data numerik. Proses encoding mengubah data kategorikal menjadi bentuk yang dapat diproses oleh algoritma.

7. **Pemisahan Data Train dan Test**:
   - Proses: Memisahkan dataset menjadi data pelatihan (train set) dan data pengujian (test set).
   - Alasan: Pemisahan ini diperlukan untuk menguji performa model pada data yang belum pernah dilihat sebelumnya dan menghindari overfitting.

8. **Standardisasi/Scaling Nilai Numerik**:
   - Proses: Melakukan scaling atau standardisasi pada nilai-nilai numerik dalam dataset.
   - Alasan: Scaling memastikan bahwa nilai-nilai numerik memiliki skala yang serupa, sehingga algoritma yang sensitif terhadap skala dapat beroperasi dengan baik.

## Modeling
Pada tahap pemodelan, telah digunakan beberapa algoritma machine learning untuk membangun model prediksi risiko serangan jantung. Algoritma yang dipilih adalah sebagai berikut:

1. **Logistic Regression**:
   - Algoritma ini dipilih sebagai model baseline karena kemampuannya dalam mengatasi masalah klasifikasi.
   - Parameter yang digunakan adalah default dari library scikit-learn.

2. **Random Forest Classifier**:
   - Algoritma ini dipilih untuk melihat apakah model ensemble dapat memberikan hasil yang lebih baik.
   - Parameter yang digunakan juga adalah default dari scikit-learn.

3. **Decision Tree Classifier**:
   - Algoritma ini digunakan untuk melihat kinerja model berbasis decision tree.
   - Parameter yang digunakan adalah default dari scikit-learn.

4. **Gradient Boosting Classifier**:
   - Algoritma ini dipilih karena kemampuannya dalam meningkatkan akurasi model dengan cara memadukan banyak model lemah.
   - Parameter yang digunakan adalah default dari scikit-learn.

5. **K-Nearest Neighbors (KNN)**:
   - Algoritma ini digunakan untuk melihat bagaimana model berbasis pengelompokan berkinerja dalam permasalahan ini.
   - Parameter yang digunakan adalah default dari scikit-learn.

Selama proses pemodelan,  dataset yang digunakan telah dilakukan preprocessing sedemikian rupa dan dibagi menjadi data train dan test. Setiap algoritma diterapkan pada data train, dan hasilnya dievaluasi dengan menggunakan berbagai metrik evaluasi, termasuk akurasi, precision, recall, dan f1-score.

Hasil pemodelan menunjukkan bahwa model terbaik yang dipilih adalah **Logistic Regression** dengan akurasi 0.6418. Model ini dipilih karena mampu mengidentifikasi individu yang tidak memiliki risiko serangan jantung dengan cukup baik. Meskipun recall untuk kelas "Heart Attack" rendah, model ini masih memberikan hasil yang baik secara keseluruhan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
**Kelebihan dan Kekurangan Algoritma:**

1. **Random Forest Classifier**:
   - *Kelebihan*:
     - Mampu menangani sejumlah besar fitur dengan baik.
     - Tidak sensitif terhadap data yang tidak seimbang.
     - Mampu menangani data kategorikal tanpa perlu encoding.
     - Rentan terhadap overfitting.
     - Menghasilkan feature importance untuk membantu interpretasi model.
   - *Kekurangan*:
     - Kemungkinan terlalu kompleks untuk data yang sederhana.
     - Memerlukan waktu lebih lama untuk melatih model dibandingkan dengan beberapa algoritma lainnya.

2. **Logistic Regression**:
   - *Kelebihan*:
     - Sederhana dan mudah diinterpretasi.
     - Cepat dilatih dan cocok untuk dataset kecil hingga sedang.
     - Cocok untuk masalah klasifikasi biner.
   - *Kekurangan*:
     - Kurang efektif ketika hubungan antara fitur dan target tidak linier.
     - Tidak dapat menangani interaksi antara fitur dengan baik.

3. **Decision Tree Classifier**:
   - *Kelebihan*:
     - Mudah diinterpretasi dan dapat divisualisasikan.
     - Cocok untuk data kategorikal.
     - Mampu menangani sejumlah besar fitur dengan baik.
   - *Kekurangan*:
     - Cenderung overfitting jika tidak ada pengaturan yang tepat.
     - Tidak stabil terhadap perubahan kecil dalam data pelatihan.

4. **Gradient Boosting Classifier**:
   - *Kelebihan*:
     - Menghasilkan model yang kuat dengan tingkat akurasi yang tinggi.
     - Dapat menangani masalah regresi dan klasifikasi.
   - *Kekurangan*:
     - Memerlukan waktu pelatihan yang lebih lama.
     - Rentan terhadap overfitting jika tidak ada pengaturan yang tepat.

5. **K-Nearest Neighbors (KNN)**:
   - *Kelebihan*:
     - Sederhana dan mudah dipahami.
     - Cocok untuk masalah klasifikasi dan regresi.
   - *Kekurangan*:
     - Rentan terhadap pengaruh outlier.
     - Memerlukan waktu komputasi yang tinggi untuk menghitung jarak antara titik data.

**Pemilihan Model Terbaik:**
 <img src="Images/model.png" alt="model" width="auto" height="auto"> <br>
Model terbaik, yaitu **Logistic Regression**, dipilih berdasarkan akurasi tertinggi (0.6418) dan precision yang tinggi untuk kelas mayoritas ("No Heart Attack"). Model ini dapat mengidentifikasi individu yang tidak memiliki risiko serangan jantung dengan sangat baik. Meskipun recall untuk kelas "Heart Attack" rendah, model ini masih memberikan hasil yang baik dalam hal akurasi dan precision secara keseluruhan.


## Evaluation
Model-model yang diuji termasuk **Random Forest**, **Logistic Regression**, **Decision Tree**, **Gradient Boosting**, dan **K-Nearest Neighbors**. Hasil menunjukkan bahwa masing-masing model memiliki kinerja yang berbeda. Sebagai contoh, model** Logistic Regression** memiliki akurasi tertinggi sekitar 0,6418, tetapi memiliki nilai recall yang rendah untuk kasus **Serangan Jantung**. Metrik evaluasi memberikan gambaran yang lengkap tentang kinerja model. Namun, pemilihan model terbaik akan bergantung pada prioritas yang berbeda, misalnya, apakah kita lebih peduli dengan presisi, recall, akurasi, atau bahkan semuanya. Akurasi keseluruhan model berada di sekitar 53% hingga 64%, yang berarti sekitar 53% hingga 64% dari semua kasus diprediksi dengan benar. Dengan demikian, hasil proyek dapat dinilai berdasarkan metrik evaluasi ini untuk menentukan model yang paling sesuai untuk memprediksi risiko serangan jantung.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- **Akurasi (Accuracy)**:
   - Formula: (TP + TN) / (TP + TN + FP + FN)
   - Akurasi mengukur sejauh mana model dapat memprediksi dengan benar baik kelas positif (Heart Attack) maupun kelas negatif (No Heart Attack). Ini adalah rasio dari prediksi yang benar dibandingkan dengan semua prediksi.
- **Presisi (Precision)**:
   - Formula: TP / (TP + FP)
   - Presisi mengukur sejauh mana prediksi positif yang dibuat oleh model benar. Ini menghitung rasio antara True Positives (kasus yang benar-benar termasuk dalam kelas positif) dengan semua prediksi positif yang dibuat. 
- **Recall (Sensitivitas atau True Positive Rate)**:
    - Formula: TP / (TP + FN)
    - Recall mengukur sejauh mana model dapat mengidentifikasi semua kasus positif yang sebenarnya. Ini menghitung rasio antara True Positives (kasus yang benar-benar termasuk dalam kelas positif) dengan semua kasus positif yang 
      sebenarnya.
-**F1-Score**:
  - Formula: 2 * (Presisi * Recall) / (Presisi + Recall)
  - F1-Score adalah metrik yang menggabungkan presisi dan recall. Ini memberikan gambaran tentang keseimbangan antara akurasi model dalam mengidentifikasi kasus positif dan kemampuannya dalam menghindari kesalahan positif.

**---Ini adalah bagian akhir laporan---**

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
- Menambahkan bagian “Solution Statement” yang menguraikan cara untuk meraih goals. Bagian ini dibuat dengan ketentuan sebagai berikut: 

    ### Solution statements
    - Mengajukan 2 atau lebih solution statement. Misalnya, menggunakan dua atau lebih algoritma untuk mencapai solusi yang diinginkan atau melakukan improvement pada baseline model dengan hyperparameter tuning.
    - Solusi yang diberikan harus dapat terukur dengan metrik evaluasi.

## Data Understanding
Paragraf awal bagian ini menjelaskan informasi mengenai data yang Anda gunakan dalam proyek. Sertakan juga sumber atau tautan untuk mengunduh dataset. Contoh: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Restaurant+%26+consumer+data).

Selanjutnya uraikanlah seluruh variabel atau fitur pada data. Sebagai contoh:  

### Variabel-variabel pada Restaurant UCI dataset adalah sebagai berikut:
- accepts : merupakan jenis pembayaran yang diterima pada restoran tertentu.
- cuisine : merupakan jenis masakan yang disajikan pada restoran.
- dst

**Rubrik/Kriteria Tambahan (Opsional)**:
- Melakukan beberapa tahapan yang diperlukan untuk memahami data, contohnya teknik visualisasi data atau exploratory data analysis.

## Data Preparation
Pada bagian ini Anda menerapkan dan menyebutkan teknik data preparation yang dilakukan. Teknik yang digunakan pada notebook dan laporan harus berurutan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan proses data preparation yang dilakukan
- Menjelaskan alasan mengapa diperlukan tahapan data preparation tersebut.

## Modeling
Tahapan ini membahas mengenai model machine learning yang digunakan untuk menyelesaikan permasalahan. Anda perlu menjelaskan tahapan dan parameter yang digunakan pada proses pemodelan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan kelebihan dan kekurangan dari setiap algoritma yang digunakan.
- Jika menggunakan satu algoritma pada solution statement, lakukan proses improvement terhadap model dengan hyperparameter tuning. **Jelaskan proses improvement yang dilakukan**.
- Jika menggunakan dua atau lebih algoritma pada solution statement, maka pilih model terbaik sebagai solusi. **Jelaskan mengapa memilih model tersebut sebagai model terbaik**.

## Evaluation
Pada bagian ini anda perlu menyebutkan metrik evaluasi yang digunakan. Lalu anda perlu menjelaskan hasil proyek berdasarkan metrik evaluasi yang digunakan.

Sebagai contoh, Anda memiih kasus klasifikasi dan menggunakan metrik **akurasi, precision, recall, dan F1 score**. Jelaskan mengenai beberapa hal berikut:
- Penjelasan mengenai metrik yang digunakan
- Menjelaskan hasil proyek berdasarkan metrik evaluasi

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.

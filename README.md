# Oral Cancer Prediction Model

## Ringkasan Proyek
Proyek ini bertujuan untuk membangun model prediktif dalam mendiagnosis kanker mulut menggunakan data pasien. Dua algoritma pembelajaran mesin digunakan dalam proyek ini: Logistic Regression dan Random Forest. Dataset mencakup faktor risiko, gejala, dan informasi pengobatan untuk mendukung deteksi dini dan pengambilan keputusan dalam perawatan kanker.

## Fitur Utama
- **Model Prediksi:** Menggunakan Logistic Regression dan Random Forest untuk klasifikasi.
- **Analisis Feature Importance:** Mengidentifikasi faktor-faktor yang paling memengaruhi prediksi (khusus untuk Random Forest).
- **Metode Evaluasi:** Evaluasi kinerja model secara menyeluruh menggunakan precision, recall, F1-score, dan akurasi.
- **Visualisasi:** Menyertakan plot feature importance untuk interpretasi lebih baik (hanya pada Random Forest).

## Deskripsi Dataset
Dataset ini mencakup data global tentang kanker mulut, dengan fokus pada:
- **Demografi:** Usia, jenis kelamin, dan negara.
- **Faktor Risiko:** Penggunaan tembakau, konsumsi alkohol, infeksi HPV, dan penggunaan pinang.
- **Gejala:** Ukuran tumor, kesulitan menelan, lesi mulut, dan perdarahan yang tidak dijelaskan.
- **Detail Pengobatan:** Jenis pengobatan dan biaya terkait.
- **Hasil:** Tingkat kelangsungan hidup dan beban ekonomi.

### Kolom
- Demografi: `Usia`, `Negara`, `Jenis Kelamin`
- Faktor Risiko: `Penggunaan Tembakau`, `Konsumsi Alkohol`, `Infeksi HPV`, `Penggunaan Pinang`
- Gejala: `Ukuran Tumor`, `Stadium Kanker`, `Lesi Putih atau Merah di Mulut`
- Target: `Diagnosa Kanker Mulut`

## Alur Proyek
### 1. Pra-pemrosesan Data
- Membersihkan data dan menangani nilai yang hilang.
- Encoding variabel kategorikal dan standarisasi fitur numerik.

### 2. Pembangunan Model
- **Algoritma:**
  - Logistic Regression: Sebagai model baseline untuk klasifikasi.
  - Random Forest: Sebagai model yang lebih kompleks dengan kemampuan untuk menghitung feature importance.
- **Tuning Hyperparameter:** 
  - Logistic Regression: Parameter seperti `penalty` dan `C`.
  - Random Forest: Parameter seperti `max_depth`, `n_estimators`, dan `min_samples_split`.

### 3. Analisis Feature Importance (Random Forest)
- Menggunakan fungsi `mean_score_decrease` untuk menganalisis feature importance.
- Visualisasi fitur-fitur yang paling penting.

### 4. Evaluasi Model
- Menggunakan metrik: Precision, Recall, F1-score, dan Akurasi.
- Laporan dihasilkan untuk kedua algoritma menggunakan fungsi `classification_report` dari sklearn.

### Contoh Insight dari Feature Importance (Random Forest)
1. **Stadium Kanker:** Memberikan kontribusi ~45.3%, menekankan pentingnya deteksi dini dan penentuan stadium.
2. **Tanpa Pengobatan:** Mengindikasikan hasil yang signifikan untuk pasien tanpa pengobatan (~32%).
3. **Faktor Risiko:** Pengaruh sedang dari jenis pengobatan seperti pembedahan, radiasi, dan kemoterapi.

## Hasil
- **Kinerja Model:**
  - Logistic Regression: Memberikan baseline performa dengan hasil evaluasi yang memadai.
  - Random Forest: Mencapai akurasi 100% pada data uji, namun validasi lebih lanjut disarankan menggunakan dataset eksternal.
- **Feature Importance (khusus Random Forest):** Memvisualisasi faktor terpenting untuk interpretasi model yang lebih baik.



## 🌊 Klasifikasi Status Ketersediaan Air Bersih dengan Random Forest 🌊

Selamat datang di proyek UTS untuk mata kuliah Aplikasi Pembelajaran Mesin! Proyek ini menunjukkan bagaimana Random Forest digunakan untuk mengklasifikasikan status ketersediaan air bersih menjadi Aman, Sedang, atau Kritis dengan akurasi luar biasa 98,66%! 🚀 Dataset dummy dibuat menggunakan AI untuk simulasi realistis, dan hasilnya dievaluasi dengan confusion matrix untuk melihat performa model. 

## 📖 Latar Belakang

Air bersih adalah kebutuhan dasar, tapi banyak daerah menghadapi krisis karena polusi, kekeringan, atau pipa rusak. Dengan Random Forest, kita bisa prediksi status air bersih (Aman, Sedang, Kritis) berdasarkan data seperti curah hujan, polutan, dan lainnya. Ini bantu pemerintah, PDAM, dan warga atasi masalah air lebih cepat!

## 📊 Dataset Dummy

Kami membuat dataset dummy dengan 20 record menggunakan AI untuk simulasi realistis. Dataset ini punya:



Fitur (7): Curah Hujan (mm), Kadar Polutan (mg/L), Debit Air (m³/s), Suhu Udara (°C), Kepadatan Penduduk (jiwa/km²), Konsumsi Air (liter/kapita), Status Infrastruktur (%).

Label: Status Ketersediaan Air (Aman, Sedang, Kritis).

## 🛠️ Cara Kerja Model

Kami menggunakan Random Forest dari library scikit-learn di Python untuk mengklasifikasikan status ketersediaan air bersih. Berikut langkah-langkah yang dilakukan:

1. **Preprocessing Data:**
   - Label pada kolom `Status Ketersediaan Air` diubah menjadi angka menggunakan `LabelEncoder`.
   - Fitur (`X`) dipisahkan dari label (`y`).

2. **Membagi Data:**
   - Data dibagi menjadi 70% data latih dan 30% data uji menggunakan `train_test_split` dengan stratifikasi label.

3. **Menyeimbangkan Data:**
   - Data latih diseimbangkan menggunakan teknik SMOTE agar kelas seimbang dan model tidak bias.

4. **Membangun Model:**
   - Model Random Forest dibangun dengan parameter:
     - `n_estimators=100`
     - `class_weight='balanced'`
     - `random_state=42`
     - `n_jobs=-1` (mempercepat proses training dengan semua core)

5. **Melatih Model:**
   - Model dilatih menggunakan data latih hasil SMOTE.

6. **Prediksi dan Evaluasi:**
   - Model memprediksi data uji.
   - Hasil prediksi dan label aktual dikembalikan ke format aslinya menggunakan `inverse_transform`.

7. **Evaluasi Akurasi:**
   - Menghitung akurasi model menggunakan `accuracy_score`.
   - Menampilkan classification report (precision, recall, f1-score).

8. **Confusion Matrix:**
   - Menampilkan confusion matrix untuk melihat performa klasifikasi antar label.

9. **Feature Importances:**
   - Menampilkan fitur-fitur yang paling berpengaruh dalam proses klasifikasi berdasarkan nilai pentingnya dari model.



## 🎯 Hasil
Akurasi: 98,66%! Model sangat akurat dalam prediksi status air bersih.

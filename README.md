## 🌊 Klasifikasi Status Ketersediaan Air Bersih dengan Random Forest 🌊

Selamat datang di proyek UTS untuk mata kuliah Aplikasi Pembelajaran Mesin! Proyek ini menunjukkan bagaimana Random Forest digunakan untuk mengklasifikasikan status ketersediaan air bersih menjadi Aman, Sedang, atau Kritis dengan akurasi luar biasa 98,66%! 🚀 Dataset dummy dibuat menggunakan AI untuk simulasi realistis, dan hasilnya dievaluasi dengan confusion matrix untuk melihat performa model. 

## 📖 Latar Belakang

Air bersih adalah kebutuhan dasar, tapi banyak daerah menghadapi krisis karena polusi, kekeringan, atau pipa rusak. Dengan Random Forest, kita bisa prediksi status air bersih (Aman, Sedang, Kritis) berdasarkan data seperti curah hujan, polutan, dan lainnya. Ini bantu pemerintah, PDAM, dan warga atasi masalah air lebih cepat!

## 📊 Dataset Dummy

Kami membuat dataset dummy dengan 20 record menggunakan AI untuk simulasi realistis. Dataset ini punya:



Fitur (7): Curah Hujan (mm), Kadar Polutan (mg/L), Debit Air (m³/s), Suhu Udara (°C), Kepadatan Penduduk (jiwa/km²), Konsumsi Air (liter/kapita), Status Infrastruktur (%).

Label: Status Ketersediaan Air (Aman, Sedang, Kritis).

## 🛠️ Cara Kerja Model

Kami menggunakan Random Forest dari library scikit-learn di Python untuk klasifikasi.  
Langkah-langkahnya:

- **Buat Data Dummy:** 1000 record dengan fitur dan label.
- **Pisah Data:** 70% untuk latih, 30% untuk uji
- **Latih Model:** Random Forest dengan 100 pohon (`n_estimators=100`) untuk akurasi tinggi.
- **Evaluasi:** Hitung akurasi dan buat confusion matrix untuk melihat performa.

## 🎯 Hasil
Akurasi: 98,66%! Model sangat akurat dalam prediksi status air bersih.

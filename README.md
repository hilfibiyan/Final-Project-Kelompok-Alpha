# Proyek Akhir - Prediksi Pembatalan Pemesanan Hotel

## Judul Proyek
**Memprediksi Pembatalan Pemesanan Hotel untuk Mendukung Strategi Dynamic Pricing dan Overbooking**

## Anggota Kelompok
1. Hilfi Biyan Firza (JCDSOL-018-039)  
2. Andhik Surya Saputra (JCDSOL-018-028)  
3. Fauzan Akmal Baihaqi (JCDSOL-018-038)

---

## Ringkasan Permasalahan

### Konteks Bisnis
Industri perhotelan menghadapi tantangan besar terkait tingginya tingkat pembatalan pemesanan. Berdasarkan data dari [D-Edge Hospitality Solution](https://www.hotelmanagement.net/tech/study-cancelation-rate-at-40-as-otas-push-free-change-policy), tingkat pembatalan meningkat dari **32,9% pada tahun 2014** menjadi **39,6% pada tahun 2018**.

Tingginya pembatalan ini berdampak pada pendapatan hotel, terutama jika terjadi mendekati tanggal kedatangan, sehingga kamar yang dibatalkan tidak sempat dijual kembali. Strategi overbooking memang bisa digunakan, namun berisiko membuat tamu kecewa karena tidak mendapatkan kamar saat datang.

### Rumusan Masalah
Hotel membutuhkan model prediksi untuk mengidentifikasi potensi pembatalan sejak awal. Hal ini akan mendukung:
- Strategi overbooking yang lebih optimal
- Keputusan harga yang dinamis (dynamic pricing)
- Pemberian insentif yang sesuai dengan segmen pelanggan

---

## Tujuan
- Membangun model prediktif untuk memprediksi pembatalan pemesanan dengan akurasi tinggi.
- Mengidentifikasi faktor utama yang memengaruhi pembatalan (seperti lead_time, deposit_type, market_segment).
- Merancang strategi bisnis seperti dynamic pricing dan overbooking terkendali untuk meminimalkan kerugian akibat pembatalan.

---

## Dataset

- Sumber: Kaggle
- Periode: Juli 2015 - Agustus 2017
- Lokasi: Resort Hotel (Algarve) dan City Hotel (Lisbon), Portugal
- Jumlah Baris: Tidak disebutkan secara eksplisit, tetapi mencakup data pemesanan dengan fitur lengkap.
- Fitur Utama:
  - is_canceled: Target (0: Tidak dibatalkan, 1: Dibatalkan)
  - lead_time: Jumlah hari antara pemesanan dan kedatangan
  - deposit_type: Jenis deposit (No Deposit, Non Refund, Refundable)
  - market_segment: Segmen pasar (Online TA, Direct, Groups, dll.)
  - adr: Average Daily Rate (tarif rata-rata harian)
  - Lihat notebook untuk daftar lengkap 32 atribut.

---

## Metodologi
- **Pra-pemrosesan Data**: Pembersihan data, rekayasa fitur, dan EDA
- **Modeling**: Logistic Regression, Random Forest, XGBoost, dll.
- **Evaluasi**: ROC-AUC, Akurasi, Precision, Recall, F1-Score
- **Deployment**: Aplikasi Streamlit

---

## EDA dan Insight

- City Hotel memiliki tingkat pembatalan yang lebih tinggi dibandingkan Resort Hotel.
- Pelanggan dengan status “non-refundable” cenderung tidak membatalkan.
- Tamu dengan harga kamar lebih tinggi (adr tinggi) memiliki kemungkinan pembatalan lebih besar.
- Pelanggan bertipe `Transient` mendominasi dan cenderung lebih sering membatalkan.

---

## Modelling

Model yang diuji:
- Logistic Regression
- Decision Tree
- Random Forest
- **XGBoost (model terbaik)**

Evaluasi dilakukan dengan:
- Train-test split
- Confusion Matrix
- Classification Report
- ROC Curve & AUC Score
- Hyperparameter tuning menggunakan GridSearchCV

---

## Hasil Model

- **XGBoost** memberikan performa terbaik dengan ROC AUC mencapai >90%.
- Recall dan Precision cukup tinggi untuk mendeteksi kelas "cancel".
- Model mampu membantu hotel mengantisipasi pembatalan lebih dini.
- Fitur Penting:
  - required_car_parking_spaces: Tamu yang meminta parkir cenderung tidak membatalkan.
  - deposit_type_Non Refund: Kebijakan non-refunded mengurangi pembatalan.
  - previous_cancellations: Riwayat pembatalan meningkatkan risiko.
  - market_segment_Online TA: Segmen OTA memiliki risiko pembatalan tinggi.

---

## Tableau Dashboard

**Link**: [[Link Tableau Public](https://public.tableau.com/views/Book1_17442929001870/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)]  
**Screenshot**:  
![Screenshot Tableau Dashboard](https://github.com/hilfibiyan/Final-Project-Kelompok-Alpha/blob/main/image.png)

---

## Struktur Repository

```
├── Alpha Group - Final Project.ipynb     # Notebook utama
├── data/                                 # Folder dataset
├── images/                               # Screenshot atau aset visual
├── README.md                             # File README ini
```

---

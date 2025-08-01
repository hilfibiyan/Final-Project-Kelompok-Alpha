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
- Membangun model machine learning untuk memprediksi pembatalan pemesanan
- Menyajikan visualisasi insight melalui Tableau Dashboard
- Mendeploy model melalui aplikasi web berbasis Streamlit

---

## Metodologi
- **Pra-pemrosesan Data**: Pembersihan data, rekayasa fitur, dan EDA
- **Modeling**: Logistic Regression, Random Forest, XGBoost, dll.
- **Evaluasi**: ROC-AUC, Akurasi, Precision, Recall, F1-Score
- **Deployment**: Aplikasi Streamlit

---

## Tableau Dashboard

**Link**: [[Link Tableau Public](https://public.tableau.com/views/Book1_17442929001870/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)]  
**Screenshot**:  
[Screenshot Tableau Dashboard](image.png)

---

## Struktur Repository

```
├── Alpha Group - Final Project.ipynb     # Notebook utama
├── data/                                 # Folder dataset
├── images/                               # Screenshot atau aset visual
├── README.md                             # File README ini
```

---

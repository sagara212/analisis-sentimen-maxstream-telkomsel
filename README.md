# 🔍 **Analisis Sentimen Ulasan Aplikasi Maxstream (Tekomsel) Menggunakan ML dan LSTM**

Proyek ini bertujuan untuk menganalisis sentimen pengguna terhadap layanan Maxstream dengan menggunakan algoritma Machine Learning (ML) dan model Neural Network (NN). Kami mengevaluasi bagaimana opini publik terhadap Maxstream yang didapat dari data komentar dan ulasan.

---

## 📂 **Dataset**

**Sumber Data**: Data dikumpulkan dari ulasan aplikasi Maxstream di Google Play Store.

**Isi Dataset**:
- **Teks**: Ulasan dan komentar terkait pengalaman pengguna dengan layanan Maxstream.
- **Label**:
  - **1**: Sentimen positif
  - **0**: Sentimen negatif
- **Jumlah Data**:
  - **Negatif**: 57% dari total data
  - **Positif**: 43% dari total data

**Langkah Persiapan Data**:
- **Preprocessing**:
  - Tokenisasi
  - Lowercasing
  - Menghapus tanda baca dan stopwords
- **Sequencing**: Mengubah teks menjadi urutan angka dengan teknik word embedding.

---

## 🛠️ **Pemodelan dan Evaluasi**
Kami menggunakan dua model utama untuk menganalisis sentimen:

### 1. **Support Vector Machine (SVM)**
- **Akurasi**: 81.80%
- **Precision**: 81.79%
- **Recall**: 81.80%

### 2. **Long Short-Term Memory (LSTM)**
- **Epoch 10/10**  
  - **Akurasi**: 90.25%
  - **Loss**: 0.2152
  - **Precision**: 87.83%
  - **Recall**: 89.54%
  - **Validation Accuracy**: 81.14%
  - **Validation Loss**: 0.6564
  - **Validation Precision**: 77.40%
  - **Validation Recall**: 79.56%

**Langkah-Langkah**:
1. **Eksplorasi Data**: Melihat distribusi data dan pola sentimen.
2. **Feature Engineering**: Menggunakan embedding teks untuk mendukung analisis mendalam.
3. **Pelatihan Model**:
   - Melatih model SVM dengan data term frequency-inverse document frequency (TF-IDF).
   - Melatih model LSTM dengan representasi vektor teks.
4. **Evaluasi Model**: Membandingkan hasil prediksi dengan data validasi menggunakan metrik akurasi, precision, dan recall.

---

## 🏆 **Hasil**

### **Kinerja Model**
| Model | Akurasi | Precision | Recall |
|-------|---------|-----------|--------|
| SVM   | 81.80%  | 81.79%    | 81.80% |
| LSTM  | 90.25% (train), 81.14% (val) | 87.83% (train), 77.40% (val) | 89.54% (train), 79.56% (val) |

**Kesimpulan Awal**:
- Model LSTM menunjukkan performa tinggi pada data training namun perlu dioptimalkan untuk data validasi.
- Model SVM stabil dan cukup andal untuk analisis sentimen awal.

### **Distribusi Sentimen**
- **Negatif**: Mayoritas ulasan mengungkapkan ketidakpuasan terhadap kualitas layanan Maxstream.
- **Positif**: Sebagian kecil mendukung layanan dengan alasan kualitas tayangan yang menarik.

---

## 💻 **Teknologi yang Digunakan**

- **Python**: Pengolahan data dan pemodelan.
- **TensorFlow & Keras**: Membangun dan melatih model LSTM.
- **Scikit-learn**: Implementasi model SVM.
- **NLTK & SpaCy**: Preprocessing data teks.
- **Matplotlib & Seaborn**: Visualisasi hasil analisis.

---

## 📈 **Visualisasi**
Kami menyediakan grafik untuk:
- Perbandingan distribusi sentimen positif dan negatif.
- Kurva loss dan akurasi selama pelatihan LSTM.
- Confusion matrix untuk SVM dan LSTM.

---

## 🔗 **Langkah Selanjutnya**
1. **Optimasi Model LSTM**: Menggunakan hyperparameter tuning untuk meningkatkan performa pada data validasi.
2. **Analisis Lanjutan**: Mengidentifikasi tema utama dalam sentimen negatif.
3. **Penerapan**: Mengembangkan dashboard interaktif untuk memvisualisasikan hasil analisis secara real-time.

# Analisis Sentimen Ulasan Skincare Serum Retinol

Proyek ini bertujuan untuk menganalisis sentimen pengguna terhadap **produk skincare serum berbahan retinol** berdasarkan ulasan pengguna yang diperoleh melalui web scraping dari situs *Female Daily*. Analisis dilakukan untuk mengidentifikasi persepsi pengguna terkait manfaat, efektivitas, serta efek samping penggunaan retinol.

## 📌 Latar Belakang
Retinol merupakan salah satu bahan aktif populer dalam produk skincare karena manfaatnya dalam regenerasi kulit dan anti-aging. Namun, efek samping seperti iritasi dan kemerahan masih sering dilaporkan. Oleh karena itu, analisis sentimen ulasan pengguna dilakukan untuk membantu konsumen memahami pengalaman nyata pengguna lain sebelum menggunakan produk retinol.

## 🎯 Tujuan
- Mengklasifikasikan ulasan pengguna ke dalam sentimen **positif**, **netral**, dan **negatif**
- Memberikan wawasan bagi konsumen dalam memilih produk serum retinol
- Menjadi masukan bagi produsen untuk meningkatkan kualitas produk

## 📊 Dataset
- Sumber: *Female Daily*  
- Jumlah data: **1.437 ulasan**
- Atribut utama:
  - Skin Type
  - Usage Period & Purchase Point
  - Review (teks)
  - Rating (1–5)

## ⚙️ Metodologi
1. **Web Scraping** menggunakan BeautifulSoup  
2. **Pre-processing Teks**:
   - Case folding
   - Cleaning (URL, HTML, tanda baca, angka)
   - Stopwords removal (termasuk custom stopwords)
   - Normalization & stemming (Sastrawi)
3. **Labeling Sentimen**:
   - Positif: Rating 4–5  
   - Netral: Rating 3  
   - Negatif: Rating 1–2  
4. **Feature Engineering**:
   - TF-IDF
   - Word2Vec
5. **Model Klasifikasi**:
   - Multinomial Naive Bayes
   - K-Nearest Neighbors (KNN)
   - Random Forest (Balanced Random Forest)
6. **Handling Imbalance Data**:
   - SMOTE, ADASYN, undersampling
7. **Evaluasi Model**:
   - Accuracy, Precision, Recall, F1-Score
   - Confusion Matrix
   - Cross-validation

## 🧪 Hasil Singkat
- Mayoritas ulasan bersentimen **positif**
- Model berbasis **TF-IDF** menunjukkan performa paling stabil
- Ketidakseimbangan kelas berpengaruh besar pada performa kelas negatif dan netral
- Balanced Random Forest membantu meningkatkan prediksi pada kelas minoritas

## 🛠️ Tools & Library
- Python
- BeautifulSoup
- Pandas, NumPy
- Scikit-learn
- Gensim (Word2Vec)
- Sastrawi
- Imbalanced-learn
- Matplotlib & Seaborn



# E-Commerce Shipping Analysis

Proyek ini bertujuan untuk menganalisis data pengiriman dari sebuah perusahaan e-commerce dan membangun model machine learning untuk memprediksi keterlambatan pengiriman barang. Analisis dilakukan dengan pendekatan end-to-end, mulai dari pemahaman bisnis hingga interpretasi hasil model.

---

## Tujuan Analisis

- Memprediksi apakah suatu pengiriman akan **tepat waktu** atau **terlambat**.
- Mengidentifikasi **faktor-faktor utama** yang memengaruhi keterlambatan pengiriman.
- Mengukur **potensi kerugian bisnis** akibat prediksi yang salah (terutama *false negative*).
- Memberikan rekomendasi strategis untuk meningkatkan efisiensi logistik dan kepuasan pelanggan.

---

## Business Insight

- **False Negative (FN)** lebih merugikan dibanding False Positive, karena perusahaan gagal mengantisipasi keterlambatan → potensi penalti SLA, churn pelanggan, dan kompensasi → estimasi kerugian: ± **$300/pengiriman**.
- Oleh karena itu, metrik utama model adalah **Recall**, untuk meminimalkan FN sebanyak mungkin.

---

## Dataset

Dataset berasal dari [Kaggle - Customer Analytics](https://www.kaggle.com/datasets/prachi13/customer-analytics) dan berisi informasi seperti:
- Customer Rating
- Weight in grams
- Prior Purchases
- Mode of Shipment
- Warehouse Block
- Product Importance
- Gender, Discount, dll.
- 
---

## ✅ Hasil Utama

- **Recall Model:** 75% → Model berhasil mengidentifikasi 75% dari pengiriman yang benar-benar terlambat.
- **Fitur penting:** 
  - `Discount_offered` tinggi → layanan lebih cepat
  - `Weight_in_gms` ringan → proses lebih cepat
  - `Product_importance` tinggi → diprioritaskan
- **Interpretasi LIME:** Menunjukkan key driver prediksi dan memperkuat pemahaman pengguna terhadap output model.

---

## ⚠️ Limitasi

- Tidak mempertimbangkan data real-time seperti cuaca, kemacetan, dan gangguan logistik.
- Kualitas dan kelengkapan data sangat memengaruhi hasil model.
- Model statis dan perlu retraining berkala untuk mempertahankan performa.
- Generalisasi model ke e-commerce lain perlu validasi ulang.

---

## 📌 Rekomendasi

- Gunakan model ini dalam sistem operasional untuk mendeteksi keterlambatan sedini mungkin.
- Prioritaskan pengiriman untuk produk penting dan pelanggan baru.
- Lakukan audit terhadap gudang dan jalur pengiriman dengan performa rendah.
- Kombinasikan analisis ini dengan data eksternal untuk meningkatkan prediksi.


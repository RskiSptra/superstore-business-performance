# 📊 Superstore Business Performance & Profit Diagnosis

Proyek ini merupakan analisis bisnis komprehensif (*End-to-End*) yang bertujuan untuk mengevaluasi kinerja penjualan (*sales*) serta mendiagnosis akar penyebab kebocoran profit (*profit leakage*) pada jaringan Superstore periode 2021–2024.

Fokus utama analisis ini adalah membongkar anomali di mana volume penjualan yang tinggi tidak selalu menghasilkan margin keuntungan yang sehat, serta merumuskan rekomendasi kebijakan diskon berbasis data.

---

## 🛠️ Tech Stack & Tools
* **Data Cleaning & Preparation:** Google Sheets (`QUERY`, `XLOOKUP`, `Pivot Table`)
* **Data Visualization & Storytelling:** Google Looker Studio (2-Page Interactive Dashboard)

---

## 📖 Ringkasan Eksekutif (Executive Summary)
Secara keseluruhan, Superstore mencatatkan **Total Sales sebesar $2.30M** dengan **Total Profit $286K** (Margin 12.5%). Meskipun tren penjualan tumbuh relatif stabil, pertumbuhan ini diiringi oleh fluktuasi profit yang tidak merata di berbagai kategori dan wilayah, puncaknya terlihat pada penurunan profit drastis di bulan September.

---

## 🔍 Temuan Utama & Diagnosis Masalah

### 1. Performa Wilayah yang Timpang
* **Top 5 Profit Cities:** New York City ($62K+), Los Angeles, Seattle, San Francisco, dan Detroit menjadi penyumbang profitabilitas utama.
* **Bottom 5 Profit Cities (Merugi):** Philadelphia (-$14K+), Houston, San Antonio, Lancaster, dan Chicago mencatatkan kerugian terbesar akibat penerapan rata-rata diskon yang sangat agresif (mencapai **33–38%**).

### 2. Akar Masalah: "Jebakan Diskon >20%"
Berdasarkan segmentasi tingkat diskon (*Profit by Discount Level*), ditemukan pola kebocoran profit yang sangat jelas:
* Transaksi dengan **diskon 0–20%** terbukti aman dan menghasilkan profit yang sangat sehat.
* Begitu diskon menyentuh angka **di atas 20% (terutama 20–40% hingga >60%)**, perusahaan langsung mengalami kerugian bersih (*net loss*).

### 3. Kategori Produk Kritis
* Produk seperti *Tables*, *Bookcases*, dan *Supplies* menjadi penyumbang kerugian terbesar akibat pemotongan harga yang tidak terkontrol.
* Sebaliknya, *Copiers* dan *Paper* menjadi tulang punggung profitabilitas dengan margin di atas 35% berkat minimnya obral diskon.

---

## 💡 Rekomendasi Tindakan (Actionable Insights)

1. **Batasi Diskon Maksimal 20%:** Terapkan batas maksimal (*cap*) diskon 20% untuk kategori bermasalah (*Tables*, *Bookcases*, *Supplies*).
2. **Audit Kebijakan Cabang:** Lakukan audit terhadap kebijakan obral diskon di cabang Philadelphia, Houston, dan San Antonio.
3. **Sistem Approval Bertingkat:** Pertimbangkan penerapan sistem persetujuan (*approval*) khusus oleh Manajer Regional untuk setiap pengajuan diskon di atas 20% guna mencegah kerugian berulang.
4. **Jadikan 'Copiers' & 'Paper' sebagai Benchmark:** Terapkan strategi margin tinggi dan diskon rendah milik *Copiers* & *Paper* ke kategori produk lainnya.

---

## 📊 Interactive Dashboard (Looker Studio)

Dashboard dirancang dalam dua halaman berurutan untuk memfasilitasi *data storytelling* (Overview ➡️ Diagnosis).

### Page 1: Business Performance Overview
*Menyajikan ringkasan kesehatan bisnis, metrik utama, tren bulanan, segmentasi pelanggan, dan kinerja penjualan vs profit per sub-kategori.*

![Superstore Business Performance Overview](Picture/page1-overview.png)

---

### Page 2: Profit Diagnosis (Where and Why We're Losing Money)
*Membedah akar masalah kerugian dengan menyoroti performa kota terbawah dan korelasi langsung antara tingkat diskon dengan margin profit.*

![Profit Diagnosis](Picture/page2-diagnosis.png)

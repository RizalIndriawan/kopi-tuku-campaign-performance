# ☕ Kopi Tuku — Campaign Performance Analysis

> Analisis performa kampanye pemasaran **Kopi Tuku** sepanjang tahun 2025 (Januari–Desember), mencakup data cleaning, exploratory data analysis (EDA), perhitungan KPI, dan visualisasi dashboard.

---

## 📌 Deskripsi Project

Project ini menggunakan dataset sintetis (dummy) transaksi Kopi Tuku untuk melatih kemampuan **Data Analyst** dalam:

- **Data Cleaning** — menangani missing values, duplikat, inkonsistensi teks/tanggal, dan validasi metrik turunan
- **Exploratory Data Analysis (EDA)** — memahami pola data berdasarkan channel, campaign, kota, produk, dan segmen pelanggan
- **KPI Analysis** — menghitung dan menganalisis metrik bisnis utama
- **Dashboard** — memvisualisasikan insight dalam bentuk dashboard interaktif

---

## 📂 Struktur File

```
kopi-tuku-campaign-performance/
│
├── Dataset_raw.xlsx          # Dataset mentah (dirty) — 6.100 baris
│   ├── Dirty_Data            # Data transaksi dengan berbagai masalah kualitas data
│   ├── README                # Deskripsi singkat project & dataset
│   └── Data_Dictionary       # Penjelasan setiap kolom
│
├── Dataset_Clean.xlsx        # Dataset bersih (clean) — 4.064 baris
│   ├── Clean_Data            # Data transaksi yang sudah dibersihkan
│   ├── KPI_Summary           # Rangkuman KPI utama
│   ├── Monthly_Summary       # Performa bulanan
│   ├── Campaign_Summary      # Performa per campaign
│   ├── Channel_Summary       # Performa per channel marketing
│   ├── Product_Summary       # Performa per produk
│   └── Cleaning_Log          # Log langkah-langkah pembersihan data
│
├── Kopi_Tuku_Dashboard.pdf   # Dashboard visualisasi (PDF)
│
└── README.md                 # Dokumentasi project (file ini)
```

---

## 📊 Data Dictionary

| Kolom | Deskripsi |
|---|---|
| `Transaction_ID` | ID unik transaksi |
| `Transaction_Date` | Tanggal transaksi |
| `City` | Kota lokasi transaksi |
| `Campaign_Name` | Nama kampanye pemasaran |
| `Campaign_Type` | Tipe kampanye (Awareness, Conversion, Engagement, Retention) |
| `Marketing_Channel` | Channel pemasaran (Email, Facebook, Google Ads, Instagram, Offline, TikTok) |
| `Product` | Nama produk |
| `Size` | Ukuran produk (Regular / Large) |
| `Customer_Segment` | Segmen pelanggan (New Customer / Returning Customer) |
| `Payment_Method` | Metode pembayaran |
| `Quantity` | Jumlah item per transaksi |
| `Discount_Pct` | Persentase diskon (%) |
| `Ad_Spend` | Biaya iklan (IDR) |
| `Impressions` | Jumlah impresi iklan |
| `Clicks` | Jumlah klik iklan |
| `Leads` | Jumlah leads yang dihasilkan |
| `Conversions` | Jumlah konversi |
| `Unit_Price` | Harga satuan produk (IDR) |
| `Gross_Revenue` | Pendapatan kotor sebelum diskon (IDR) |
| `Discount_Amount` | Nilai potongan diskon (IDR) |
| `Net_Revenue` | Pendapatan bersih setelah diskon (IDR) |
| `COGS` | Cost of Goods Sold (IDR) |
| `Profit` | Profit / keuntungan (IDR) |
| `ROAS` | Return on Ad Spend |

---

## 🎯 KPI Summary

| KPI | Nilai |
|---|---|
| **Total Revenue** | Rp 193.915.996 |
| **Total Ad Spend** | Rp 558.122.544 |
| **Total Profit** | Rp 106.871.060 |
| **Total Orders** | 4.064 |
| **Total Conversions** | 573.301 |
| **AOV (Average Order Value)** | Rp 47.716 |
| **ROAS** | 0,35 |
| **CTR (Click-Through Rate)** | 10,40% |
| **Conversion Rate** | 25,29% |

---

## 🧹 Data Cleaning Process

Langkah-langkah pembersihan data yang dilakukan:

| Step | Detail |
|---|---|
| Raw rows | 6.100 baris |
| Duplikat exact dihapus | 100 baris |
| Record basic invalid dihapus | 284 baris |
| Record funnel invalid dihapus | 1.652 baris |
| **Final cleaned rows** | **4.064 baris** |
| Missing kategorikal | Diisi dengan **mode** |
| Missing numerik | Diisi dengan **median** |
| Metrik turunan | Dihitung ulang (Gross Revenue, Discount Amount, Net Revenue, COGS, Profit, ROAS, CTR, Lead Rate, Conversion Rate, AOV) |

---

## 🔍 Suggested KPIs & Analysis

- **Revenue & Profit**: Total Revenue, Total Profit, Profit Margin
- **Orders**: Total Orders, AOV (Average Order Value)
- **Advertising**: Ad Spend, ROAS (Return on Ad Spend)
- **Funnel**: CTR (Click-Through Rate), Conversion Rate, Lead Rate
- **Breakdown**: Top Campaign, Top Channel, Top Product, Top City

---

## 🛠 Tools yang Digunakan

- **Microsoft Excel / Google Sheets** — Data cleaning & analysis
- **Dashboard Tool** — Visualisasi data (Looker Studio / Tableau / Power BI)
- **Python (opsional)** — Untuk analisis lanjutan

---

## 🚀 Cara Menggunakan

1. **Clone** repository ini:
   ```bash
   git clone https://github.com/<username>/kopi-tuku-campaign-performance.git
   ```
2. Buka `Dataset_raw.xlsx` untuk melihat data mentah dan memulai proses cleaning sendiri
3. Bandingkan hasil cleaning Anda dengan `Dataset_Clean.xlsx`
4. Lihat `Kopi_Tuku_Dashboard.pdf` untuk referensi visualisasi dashboard

---

## 📄 Lisensi

Project ini dibuat untuk keperluan **edukasi dan portfolio**. Dataset bersifat sintetis/dummy dan tidak merepresentasikan data asli Kopi Tuku.

---

<p align="center">
  <i>Made with ☕ for Data Analytics learning</i>
</p>

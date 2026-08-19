# Campaign Marketing Performance Dashboard

# Project Overview
Proyek ini menganalisis performa kampanye pemasaran **Kopi Kenangan** selama periode Januari–Desember 2025. Tujuan utama proyek adalah mengevaluasi efektivitas biaya pemasaran, pendapatan yang dihasilkan, efisiensi setiap kampanye, serta perjalanan pelanggan dari tahap melihat iklan hingga melakukan penukaran voucher. Proses pengolahan data dilakukan menggunakan **Microsoft Excel**, sedangkan dashboard interaktif dibuat menggunakan **Google Looker Studio**.
---

## Dataset

| Kolom | Keterangan |
|---|---|
| Month | Bulan pelaksanaan kampanye |
| Campaign_Name | Nama kampanye pemasaran |
| City | Kota tempat kampanye dijalankan |
| Product | Produk yang dipromosikan |
| Campaign_Channel | Saluran pemasaran yang digunakan |
| Budget_IDR | Anggaran awal kampanye |
| Actual_Spend_IDR | Biaya aktual kampanye |
| Impressions | Jumlah iklan ditampilkan |
| Clicks | Jumlah klik yang diperoleh |
| Vouchers_Distributed | Jumlah voucher yang dibagikan |
| Vouchers_Redeemed | Jumlah voucher yang ditukarkan |
| Campaign_Revenue_IDR | Pendapatan yang dihasilkan kampanye |

---

## Cleaning Process

Proses data cleaning dilakukan menggunakan Microsoft Excel agar data siap dianalisis dan divisualisasikan.

### 1. Menghapus Data Duplikat

Data mentah memiliki beberapa baris yang tercatat lebih dari satu kali. Fitur **Remove Duplicates** digunakan untuk menghapus 60 baris duplikat sehingga jumlah data akhir menjadi 1.200 baris.

### 2. Standardisasi dan Cleaning Teks

Teks dibersihkan dari spasi tambahan, perbedaan kapitalisasi, dan karakter yang tidak diperlukan.

Contoh:

- `PAYDAY PROMO` menjadi `Payday Promo`


### 3. Memecah Satu Kolom Menjadi Beberapa Kolom

Pemisahan dilakukan menggunakan fitur **Text to Columns** di Excel.

### 4. Memperbaiki Tipe Data

Tipe data diperbaiki agar dapat dihitung dan dianalisis dengan benar.

### 5. Menyeragamkan Teks Menggunakan Replace

Fitur **Find and Replace** digunakan untuk menyeragamkan singkatan dan penamaan kategori.

Contoh:
- `IG` menjadi `Instagram`
---
## DASHBOARD
<img width="2750" height="1813" alt="Dashboard_page-0001" src="https://github.com/user-attachments/assets/6b64adb1-2f43-4f79-9794-7ff3e20795f6" />

### KPI Summary

| KPI | Pertanyaan | Hasil |
|---|---|---:|
| Total Campaign Revenue | Berapa total pendapatan dari seluruh kampanye? | **Rp48,74 miliar** |
| Total Actual Spend | Berapa total biaya aktual yang dikeluarkan? | **Rp17,95 miliar** |
| ROAS | Berapa pendapatan yang diperoleh dari setiap Rp1 biaya pemasaran? | **2,72x** |
| Voucher Redemption Rate | Berapa persentase voucher yang berhasil ditukarkan? | **28,07%** |

### Rumus KPI

```text
ROAS = Total Campaign Revenue / Total Actual Spend

Voucher Redemption Rate =
Vouchers Redeemed / Vouchers Distributed × 100%
```

### 1. Berapa total pendapatan yang dihasilkan dari seluruh kampanye?

**Visual:** KPI Scorecard – Total Campaign Revenue

**Insight:** Total pendapatan yang dihasilkan dari seluruh kampanye mencapai **Rp48,74 miliar**. Nilai tersebut menunjukkan bahwa kampanye pemasaran memberikan kontribusi pendapatan yang cukup besar selama periode analisis.

**Rekomendasi:** Pertahankan kampanye yang memiliki kontribusi revenue tinggi dan analisis lebih lanjut performanya berdasarkan produk, kota, serta saluran pemasaran. Revenue juga perlu dibandingkan dengan biaya kampanye agar keputusan tidak hanya didasarkan pada besarnya pendapatan.

---

### 2. Berapa total biaya aktual yang dikeluarkan?

**Visual:** KPI Scorecard – Total Actual Spend

**Insight:** Total biaya aktual yang digunakan untuk menjalankan seluruh kampanye mencapai **Rp17,95 miliar**. Biaya tersebut masih lebih rendah dibandingkan total revenue yang dihasilkan.

**Rekomendasi:** Lakukan pemantauan antara anggaran awal dan actual spend pada setiap kampanye. Anggaran dapat dikurangi pada kampanye yang membutuhkan biaya besar tetapi menghasilkan revenue atau ROAS rendah.

---

### 3. Seberapa efektif biaya pemasaran dalam menghasilkan pendapatan?

**Visual:** KPI Scorecard – Return on Ad Spend atau ROAS

**Insight:** Nilai ROAS keseluruhan mencapai **2,72x**. Artinya, setiap **Rp1** biaya pemasaran yang dikeluarkan mampu menghasilkan sekitar **Rp2,72 pendapatan**. Hal ini menunjukkan bahwa kampanye secara keseluruhan mampu menghasilkan revenue yang lebih besar daripada biaya pemasarannya.

**Rekomendasi:** Prioritaskan anggaran pada kampanye yang memiliki ROAS di atas rata-rata. Kampanye dengan ROAS rendah perlu dievaluasi dari sisi target audiens, saluran pemasaran, materi promosi, dan jenis penawaran.

---

### 4. Bagaimana perkembangan pendapatan setiap bulan?

**Visual:** Line Chart – Monthly Campaign Revenue Trend

**Insight:** Pendapatan mengalami fluktuasi sepanjang tahun. Revenue terendah terjadi pada **Februari sebesar Rp3,5 miliar**, sedangkan revenue tertinggi terjadi pada **Desember sebesar Rp4,7 miliar**. Performa pendapatan terlihat meningkat pada akhir tahun, terutama pada November dan Desember.

**Rekomendasi:** Tingkatkan aktivitas promosi pada periode akhir tahun karena memiliki potensi pendapatan yang lebih tinggi. Strategi kampanye yang berhasil pada Desember dapat dianalisis dan diterapkan pada bulan dengan revenue rendah, khususnya Februari dan Juni.

---

### 5. Kampanye mana yang menghasilkan pendapatan dan ROAS tertinggi?

**Visual:** Bar Chart – Top 5 Campaign by Revenue dan ROAS Analysis by Campaign

**Insight:** Kampanye **Year End Treat** menghasilkan revenue tertinggi sebesar sekitar **Rp6,6 miliar**, diikuti oleh **Buy 2 Get 1 sebesar Rp6,1 miliar**. Sementara itu, berdasarkan perhitungan ROAS per kampanye, **Bundle Hemat** memiliki ROAS tertinggi sekitar **3,30x**. Hal ini menunjukkan bahwa kampanye dengan revenue tertinggi belum tentu menjadi kampanye yang paling efisien.

**Rekomendasi:** Pertahankan Year End Treat sebagai kampanye utama untuk menghasilkan pendapatan, tetapi prioritaskan Bundle Hemat untuk efisiensi anggaran. Penentuan anggaran sebaiknya mempertimbangkan kombinasi revenue dan ROAS, bukan hanya salah satu indikator.

---

### 6. Bagaimana performa marketing funnel?

**Visual:** Funnel Chart – Impressions, Clicks, and Vouchers Redeemed

**Insight:** Marketing funnel menghasilkan sekitar **479,56 juta impressions**, **17,77 juta clicks**, dan **2,30 juta vouchers redeemed**. Hanya sekitar **3,71% impressions** yang berhasil menghasilkan klik. Penurunan terbesar terjadi dari tahap impressions menuju clicks, yang menunjukkan bahwa banyak audiens telah melihat iklan tetapi belum tertarik untuk melakukan tindakan lebih lanjut.

**Rekomendasi:** Tingkatkan click-through rate dengan memperbaiki desain iklan, headline, call-to-action, dan segmentasi audiens. Lakukan A/B testing untuk mengetahui materi iklan dan saluran pemasaran yang paling efektif.

---

### 7. Kampanye mana yang memiliki tingkat konversi tertinggi?

**Visual:** Bar Chart – Campaign Click-to-Redemption Rate

**Insight:** Kampanye **Campus Sampling** memiliki tingkat konversi tertinggi sebesar **34,32%**, diikuti oleh **Student Discount sebesar 29,84%**. Hal ini menunjukkan bahwa kampanye dengan target audiens yang lebih spesifik dan penawaran yang relevan mampu menghasilkan konversi lebih tinggi.

**Rekomendasi:** Pertahankan dan perluas Campus Sampling ke lokasi kampus lain. Strategi segmentasi yang digunakan pada Campus Sampling dan Student Discount dapat diterapkan pada kampanye lain agar penawaran lebih sesuai dengan karakteristik target pelanggan.


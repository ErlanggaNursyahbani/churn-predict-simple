# 🌀 Prediksi Churn - Perbandingan Model ML Sederhana

Proyek ini membandingkan tiga algoritma klasifikasi populer dalam memprediksi *churn* (berhentinya pelanggan) menggunakan data pelanggan dalam format tabular. Model dibangun dan diuji menggunakan Python dan pustaka *scikit-learn*.
## 👨‍💻 Kelompok Proyek

1. **Erlangga Nursyahbani** – 202243502747 - 0895328339786
2. **Kasun** – 202243502750 - 082111520866

## 📊 Dataset

Dataset yang digunakan adalah **Telco Customer Churn**, dengan langkah *preprocessing* sebagai berikut:

- Menghapus kolom `customerID` karena tidak relevan
- Mengubah `TotalCharges` menjadi numerik
- Mengisi nilai kosong dengan median
- Melakukan *Label Encoding* pada semua fitur bertipe kategorikal

## 🔧 Model yang Digunakan

- ✅ **Logistic Regression** (Model dengan performa terbaik)
- 🌲 **Random Forest Classifier**
- ⚡ **XGBoost Classifier**

Model dilatih dengan metode *train-test split* (80% data latih, 20% data uji) untuk evaluasi yang adil.

## 📈 Hasil Evaluasi Model

| Model               | Akurasi (%) | F1-Score (%) |
|--------------------|-------------|--------------|
| Logistic Regression| **81.69**   | **62.72**    |
| Random Forest      | 79.56       | 55.00        |
| XGBoost            | 79.42       | 57.23        |

### 🧠 Mengapa Logistic Regression Unggul?

- Dataset relatif kecil (**~7000 baris**), cocok untuk model linier
- Banyak fitur menunjukkan hubungan **linier** terhadap target
- Fitur kategorikal setelah encoding menjadi fitur **biner**
- Target `Churn` sedikit imbalanced (**~26%**), Logistic Regression lebih stabil tanpa tuning tambahan

## 🧪 Contoh Prediksi

Notebook juga menyertakan simulasi prediksi terhadap data pelanggan baru:

```
Pelanggan #1: Churn (Probabilitas churn: 62.83%)
Pelanggan #2: Churn (Probabilitas churn: 55.50%)
Pelanggan #3: Tidak Churn (Probabilitas churn: 6.79%)
Pelanggan #4: Tidak Churn (Probabilitas churn: 20.45%)
Pelanggan #5: Churn (Probabilitas churn: 63.81%)
```

## 📉 Visualisasi

Notebook menyertakan visualisasi perbandingan skor Akurasi dan F1-Score antar model menggunakan barplot. Jika kamu ingin menampilkannya di README, simpan grafik sebagai `model_comparison.png`, lalu tambahkan:

```markdown
![Perbandingan Model](./images/model_comparison.png)
```

## 📁 Struktur Proyek

```
churn-predict-simple/
│
├── datasets/
│   └── data.csv
├── model.ipynb
└── README.md
```

## ⚙️ Teknologi yang Digunakan

- Python
- pandas, numpy, matplotlib, seaborn
- scikit-learn
- xgboost

---

📌 _Proyek ini dibuat sebagai bagian dari tugas akhir mata kuliah **Data Mining**, sekaligus latihan praktis dalam membandingkan performa model *machine learning* pada data tabular._

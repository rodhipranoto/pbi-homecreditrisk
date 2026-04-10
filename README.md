# Credit Default Prediction (Home Credit)

## Problem Statement
Perusahaan ingin memprediksi apakah seorang nasabah berpotensi mengalami gagal bayar (default) atau tidak. Hal ini penting untuk mengurangi risiko kredit macet.

---

## Dataset
Dataset yang digunakan berasal dari Home Credit, terdiri dari:

- ±185.000 data aplikasi (train & test)
- Data historis dari berbagai tabel (installments, bureau, dll)
- Beberapa tabel memiliki jutaan baris data

---

## Data Preprocessing
Tahapan preprocessing yang dilakukan:

- Handling missing value
- Handling infinite value
- Feature engineering (Late Payment & Debt Ratio)
- One-hot encoding untuk variabel kategorikal
- Agregasi data untuk menyederhanakan relasi

---

## Exploratory Data Analysis (EDA)

### Insight 1: Late Payment Behavior
Nasabah dengan riwayat keterlambatan pembayaran memiliki risiko default lebih tinggi.

**Action:**
- Gunakan sebagai faktor utama dalam credit scoring
- Terapkan penalti untuk nasabah dengan riwayat telat bayar

---

### Insight 2: Debt to Income Ratio
Semakin tinggi rasio kredit terhadap income, semakin tinggi risiko default.

 **Action:**
- Tentukan threshold rasio maksimal
- Batasi approval untuk nasabah berisiko tinggi

---

## Modeling

Model yang digunakan:
- XGBoost Classifier

### Feature Engineering:
- `LATE_PAYMENT_mean`
- `DEBT_INCOME_RATIO`

---

## Model Performance

- **AUC: 0.77**

Model mampu membedakan nasabah berisiko dan tidak dengan baik, sehingga dapat membantu dalam pengambilan keputusan kredit.

---

## Business Recommendation

- Implementasi credit scoring berbasis machine learning
- Segmentasi nasabah berdasarkan risiko
- Pembatasan kredit untuk high-risk customer
- Monitoring perilaku pembayaran secara berkala

---

## Tech Stack

- Python
- Pandas
- Scikit-learn
- XGBoost
- Matplotlib & Seaborn

---

## Repository Structure

# 🏥 Proyek Eksperimen Sistem Machine Learning: Stroke Prediction

![Build Status](https://github.com/Ahmds20/Eksperimen_SML_Ahmad-Jazil-Faiz/actions/workflows/preprocessing.yml/badge.svg)
[![Python 3.9](https://img.shields.io/badge/python-3.9-blue.svg)](https://www.python.org/downloads/release/python-390/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-latest-orange)](https://scikit-learn.org/stable/)

Repository ini merupakan submisi akhir untuk kelas **Membangun Sistem Machine Learning**. Proyek ini berfokus pada pembangunan pipeline preprocessing data otomatis (MLOps) untuk dataset prediksi stroke, mencakup eksperimen manual hingga otomatisasi menggunakan GitHub Actions.

## 📂 Struktur Repository

Sesuai dengan standar submission, struktur folder proyek ini adalah sebagai berikut:

```text
Eksperimen_SML_Ahmad-Jazil-Faiz
├── .github
│   └── workflows
│       └── preprocessing.yml       # Konfigurasi CI/CD GitHub Actions
├── namadataset_raw
│   └── stroke.csv                  # Dataset Mentah (Raw Data)
├── preprocessing
│   ├── Eksperimen_Ahmad-Jazil-Faiz.ipynb  # Notebook Eksperimen Manual
│   ├── automate_ahmad_jazil_faiz.py       # Script Otomatisasi (Python)
│   └── namadataset_preprocessing          # Folder Output (Generated otomatis)
└── README.md
```
🚀 Fitur Utama
- Eksperimen Terstruktur: Analisis data awal (EDA) dan preprocessing dilakukan secara manual melalui Jupyter Notebook.
- Otomatisasi Script: Konversi langkah manual menjadi fungsi Python (automate_ahmad_jazil_faiz.py) yang dapat dijalankan di lingkungan produksi.
- CI/CD Pipeline (Advance): Terintegrasi dengan GitHub Actions. Setiap kali ada perubahan kode (Push), sistem akan otomatis:
- Menyiapkan lingkungan Python.
- Menjalankan script preprocessing.
- Mengembalikan dataset bersih sebagai Artifact yang siap didownload.

🛠️ Alur Preprocessing
- Script otomatisasi melakukan tahapan pembersihan data sebagai berikut:
- Data Loading: Membaca data mentah dari namadataset_raw/stroke.csv.
- Cleaning:
  - Menghapus kolom id yang tidak relevan.
  - Menghapus data duplikat.
- Handling Missing Values: Mengisi nilai kosong pada kolom bmi menggunakan nilai Median.
- Encoding: Mengubah fitur kategorikal (seperti gender, work_type) menjadi numerik menggunakan One-Hot Encoding.
- Splitting: Membagi data menjadi Training Set (80%) dan Test Set (20%) dengan metode stratified sampling.
- Scaling: Melakukan standarisasi (StandardScaler) pada fitur numerik (age, avg_glucose_level, bmi) untuk mencegah kebocoran data (data leakage).

💻 Cara Menjalankan Secara Lokal
Jika Anda ingin menjalankan proyek ini di komputer lokal Anda:
- Clone Repository
Bash
git clone [https://github.com/Ahmds20/Eksperimen_SML_Ahmad-Jazil-Faiz.git](https://github.com/Ahmds20/Eksperimen_SML_Ahmad-Jazil-Faiz.git)
cd Eksperimen_SML_Ahmad-Jazil-Faiz

- Install Dependensi
```Bash
pip install pandas numpy scikit-learn
```
- Jalankan Script Otomatisasi Pastikan Anda berada di root folder, lalu jalankan:

```Bash
python preprocessing/automate_ahmad_jazil_faiz.py
```
Cek Hasil File data yang sudah bersih akan muncul di folder: ```preprocessing/namadataset_preprocessing/```

🤖 GitHub Actions Workflow
Proyek ini telah memenuhi kriteria Advance dengan menerapkan Workflow otomatis.
- Trigger: Push ke branch main.
- Proses: Menjalankan preprocessing di server Ubuntu.
- Output: Dataset bersih (train_processed.csv & test_processed.csv) tersedia di menu Actions > Artifacts.

Author: Ahmad Jazil Faiz

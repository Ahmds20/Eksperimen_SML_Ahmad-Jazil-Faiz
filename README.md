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

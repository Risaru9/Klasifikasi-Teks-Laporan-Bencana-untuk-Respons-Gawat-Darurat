# 🚨 Intelligent Disaster Response Classifier (IDRC)

Sistem klasifikasi laporan bencana berbasis Hybrid AI (Machine Learning + Rule-Based) untuk membantu Tim SAR merespons gawat darurat lebih cepat dan akurat.

## 📌 Masalah Utama
Media sosial penuh dengan "Noise" (doa, simpati, hoaks) yang mempersulit identifikasi laporan bencana asli.

![Status](https://img.shields.io/badge/Status-Prototype-green)
![Python](https://img.shields.io/badge/Python-3.10-blue)
![Model](https://img.shields.io/badge/Model-RandomForest-orange)

## 📌 Latar Belakang (Pain Point)
Saat bencana terjadi, media sosial dibanjiri ribuan informasi. Namun, **90% isinya adalah "Noise"** (doa, simpati, hoaks, curhatan galau). Tim SAR kesulitan memilah laporan valid secara manual, memperlambat waktu respons (Golden Time).

## 💡 Solusi Kami: Hybrid Intelligence System
Kami tidak hanya mengandalkan prediksi probabilitas model semata. Kami membangun **End-to-End Pipeline** dengan pendekatan hibrida:

1.  **Layer 1: Noise Filtering (Rule-Based)**
    * Memblokir kata kunci non-urgent (misal: *"Pray for", "Semoga", "Galau"*).
    * Mencegah *False Alarm* masuk ke dashboard petugas.
2.  **Layer 2: Local Context Injection (Knowledge Base)**
    * Sistem dibekali kamus slang & idiom lokal (misal: *"Si Jago Merah"*, *"Lindu"*, *"Ciuman Aspal"*).
    * Jika keyword pasti ditemukan, Confidence Score otomatis **99%**.
3.  **Layer 3: Machine Learning (Random Forest)**
    * Menangani klasifikasi kontekstual untuk laporan yang kompleks.
    * Dilatih menggunakan strategi **Targeted Data Augmentation** (Boosting data idiom 30x) untuk mengatasi ketimpangan data (Imbalanced Data).

## 📊 Performa Model
Model dievaluasi menggunakan **Weighted F1-Score** karena data bersifat *imbalanced*.

| Metrik | Skor | Keterangan |
| :--- | :--- | :--- |
| **Accuracy** | **~99%** | Pada Data Testing |
| **F1-Score** | **~89%** | Rata-rata terbobot |
| **Stress Test** | **23/25** | Lulus uji jebakan & slang |

## 🛠️ Struktur Project (Standard Cookiecutter)
```text
├── data/               <- Dataset mentah & hasil preprocessing
├── models/             <- Model .pkl (Hybrid Packet)
├── notebooks/          <- Eksperimen training & EDA
├── src/                <- Source code preprocessing (.py)
├── outputs/            <- Bukti visual (Confusion Matrix, WordCloud)
├── requirements.txt    <- Daftar library
└── README.md           <- Dokumentasi ini
```
🚀 Cara Menjalankan (Demo)

Clone Repository ini:
Bash

```git clone [https://github.com/USERNAME_ANDA/NAMA_REPO.git](https://github.com/USERNAME_ANDA/NAMA_REPO.git)
```
Install Library:
Bash

```pip install -r requirements.txt```

Jalankan Demo Web (Gradio): Buka notebook notebooks/Final_Demo.ipynb dan jalankan cell terakhir untuk memunculkan antarmuka web.

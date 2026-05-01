# 📊 Asa Intelligence: AI-Powered Competitor Monitoring

**Asa Intelligence** adalah sistem intelijen bisnis otomatis yang dirancang untuk memantau pergerakan brand dan kompetitor secara real-time. Proyek ini menggunakan **n8n** sebagai orkestrator utama untuk menggabungkan pencarian data, analisis AI, dan pelaporan otomatis dalam format PDF.

---

## 🚀 Fitur Utama
* **Parallel Search:** Mengumpulkan berita terbaru dari Serper API untuk beberapa brand sekaligus secara efisien.
* **Share of Voice (SoV) Calculation:** Menggunakan JavaScript kustom untuk menghitung persentase dominasi brand di media.
* **AI Sentiment Analysis:** Menganalisis sentimen berita dan memberikan skor reputasi digital menggunakan Google Gemini.
* **Automated PDF Reporting:** Mengonversi hasil analisis menjadi laporan HTML profesional dan mengubahnya menjadi PDF secara otomatis.
* **Instant Distribution:** Mengirimkan laporan final langsung ke kanal Telegram dan mencatat data historis ke Google Sheets.

---

## 🛠️ Teknologi yang Digunakan
* **Automation:** [n8n](https://n8n.io/)
* **Search Engine:** [Serper.dev API](https://serper.dev/) (Google News API)
* **AI Model:** Google Gemini 1.5 Flash
* **PDF Engine:** [PDFShift](https://pdfshift.io/)
* **Database:** Google Sheets
* **Communication:** Telegram Bot API
* **Scripting:** Node.js / JavaScript (Luxon library for DateTime)

---

## 📋 Struktur Workflow
1.  **Trigger:** Berjalan secara otomatis melalui *Schedule Trigger*.
2.  **Fetch Data:** HTTP Request paralel ke Serper API untuk brand (NFA, BISA AI, Vinix7).
3.  **Data Processing:** * `Gabungkan Data`: Konsolidasi hasil pencarian.
    * `Menyiapkan Teks AI`: Ekstraksi metrik SoV dan pembersihan teks.
4.  **AI Insight:** Gemini menganalisis kelemahan, kelebihan, dan skor reputasi.
5.  **Output:** * Penyusunan laporan ke template HTML.
    * Konversi ke PDF.
    * Pengiriman Dokumen ke Telegram.

---

## 📸 Dokumentasi
<img width="1920" height="1080" alt="Workflow Asa Intelligence" src="https://github.com/user-attachments/assets/9299af6e-0dee-409d-ab20-634c56a788b1" />

---

## ⚙️ Cara Instalasi
1.  Import file `Asa_Compe.json` ke n8n Anda.
2.  Konfigurasikan **Credentials** untuk:
    * Serper API
    * Google Gemini (Google Cloud Console)
    * PDFShift API
    * Telegram Bot API
    * Google Sheets
3.  Jalankan (Execute) workflow.

---
© 2026 Asa Intelligence - Automated Business Insights.

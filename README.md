# 📚 Bank Soal Static Generator (Serverless)

Project ini adalah engine pembuat website **Bank Soal Pendidikan** yang statis, cepat, dan otomatis. Dibangun menggunakan Python untuk mengubah data soal (JSON) menjadi halaman web (HTML) dan dokumen siap cetak (.docx/Word) secara bersamaan.

Didesain khusus untuk **AdSense-ready**, **SEO Friendly**, dan **Zero Cost Hosting** (menggunakan Cloudflare Pages).

## 🔥 Fitur Utama

* **Automation:** Sekali running script, ribuan halaman HTML & file Word ter-generate.
* **Dual Output:**
    * 🌐 **HTML:** Website responsif dengan Tailwind CSS (via CDN).
    * 📄 **DOCX:** Dokumen Word rapi lengkap dengan Kunci Jawaban terpisah (untuk guru).
* **AdSense Optimized:** Slot iklan strategis (Header, Tengah Artikel, SafeLink Download).
* **Zero Database:** Tidak perlu MySQL/PostgreSQL. Semua data berbasis file (JSON).
* **Blazing Fast:** Tidak ada processing di server. Loading page < 1 detik.
* **SEO Structure:** Mendukung Breadcrumb, H1 dinamis, dan Semantic HTML.

## 🛠️ Tech Stack

* **Language:** Python 3.x
* **Library:** `python-docx` (untuk generate Word), `json`, `os`.
* **Frontend:** HTML5, Tailwind CSS (Utility-first).
* **Hosting:** Cloudflare Pages (Rekomendasi).

## 🚀 Cara Install (Setup Awal)

1.  **Clone Repository ini:**
    ```bash
    git clone [https://github.com/DHEWAYY/web_bank_soal_id.git](https://github.com/DHEWAYY/web_bank_soal_id.git)
    cd web_bank_soal_id
    ```

2.  **Install Library Python:**
    Hanya butuh satu library tambahan untuk fitur Word.
    ```bash
    pip install python-docx
    ```

## 📂 Struktur Folder

```text
.
├── data/               # Taruh file soal (JSON) disini
├── output/             # Hasil generate HTML ada disini (JANGAN DIEDIT MANUAL)
│   └── downloads/      # File .docx akan muncul disini
├── generator.py        # Script ajaib (Engine utama)
├── template.html       # Desain tampilan website
└── README.md           # Dokumentasi ini"# web_bank_soal_id"  

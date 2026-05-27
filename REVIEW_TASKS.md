# Tinjauan Codebase & Usulan Tugas

Berikut hasil tinjauan awal codebase beserta **masing-masing satu tugas** untuk kategori yang diminta.

## 1) Tugas perbaikan salah ketik (typo)
**Temuan:** Pada komentar `# --- KONFIGURASI CUAN & SEO ---`, istilah "CUAN" kurang profesional untuk konteks konfigurasi teknis dan tidak konsisten dengan komentar lain yang lebih formal.

**Tugas:** Ganti komentar menjadi istilah teknis yang konsisten, misalnya `# --- KONFIGURASI MONETISASI & SEO ---` pada `generator.py`.

**Kriteria selesai:**
- Komentar diperbarui tanpa mengubah perilaku program.
- Istilah komentar konsisten dan profesional.

## 2) Tugas perbaikan bug
**Temuan:** Fungsi JavaScript `cariSoal()` menggunakan variabel `desc` tanpa deklarasi (`var/let/const`), sehingga membuat global implicit variable dan berpotensi konflik antar-script.

**Tugas:** Deklarasikan variabel `desc` secara lokal (disarankan `const desc = ...`) di blok loop dalam template `TEMPLATE_SEARCH` pada `generator.py`.

**Kriteria selesai:**
- Tidak ada implicit global variable pada `cariSoal()`.
- Fitur pencarian tetap berfungsi normal pada halaman index dan listing jenjang.

## 3) Tugas perbaikan komentar kode / ketidaksesuaian dokumentasi
**Temuan:** README menyebut proses deployment dengan “Push folder `docs/` ke GitHub”, namun belum menegaskan bahwa generator juga menulis `docs/CNAME`, `docs/ads.txt`, dan `docs/.nojekyll` secara otomatis.

**Tugas:** Perbarui bagian "Cara Pakai" di `README.md` agar sinkron dengan perilaku aktual script generator terkait file output tambahan.

**Kriteria selesai:**
- README menjelaskan output utama dan output tambahan (`CNAME`, `ads.txt`, `.nojekyll`).
- Instruksi tetap singkat dan mudah diikuti pengguna baru.

## 4) Tugas peningkatan pengujian
**Temuan:** Belum ada test otomatis untuk fungsi utilitas kunci seperti `minify_html()` dan `get_badge_color()`.

**Tugas:** Tambahkan unit test Python (mis. `tests/test_generator.py`) untuk:
- `minify_html()` pada kasus whitespace antar tag.
- `get_badge_color()` untuk input jenjang SD/SMP/SMK/default.

**Kriteria selesai:**
- Seluruh test dapat dijalankan via `python -m unittest` atau `pytest`.
- Ada cakupan minimum untuk fungsi utilitas yang paling sering dipakai.

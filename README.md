# Dashboard Produksi Kelapa Sawit — PT. KJW

Dashboard produksi kelapa sawit berbasis web (single-file HTML). Mencatat data produksi harian, memantau indikator mutu laboratorium, rekap bulanan, dan konfigurasi standar mutu — semua berjalan langsung di browser tanpa server.

## Fitur

- **Login** — akses dasbor dilindungi username & password.
- **Overview** — KPI, grafik tren produksi, komposisi hasil olah, rekap bulanan, indikator mutu.
- **Produksi Harian** — input, ubah, dan hapus data produksi harian (TBS, CPO, kernel, jam operasi, FFA).
- **Laboratorium** — indikator mutu, tren FFA harian, riwayat uji lab yang bisa dicari.
- **Rekap Bulanan** — tabel rekap seluruh bulan dengan total, grafik TBS & OER per bulan, ekspor CSV.
- **Konfigurasi** — atur ambang standar mutu (FFA CPO, FFA Kernel, target KER, kapasitas olah), ekspor/impor data (JSON), hapus seluruh data.

## Cara menjalankan

Buka `index.html` langsung di browser — tidak perlu instalasi apa pun. Data tersimpan otomatis di `localStorage` browser yang digunakan.

## Live demo (GitHub Pages)

Setelah repository ini diaktifkan lewat GitHub Pages (lihat langkah di bawah), dasbor bisa diakses lewat:

```
https://<username-anda>.github.io/<nama-repo>/
```

## Login default

| Username | Password |
|---|---|
| Ryan Ade Nugraha | KJW |

> ⚠️ Kredensial ini tertanam langsung di kode (`index.html`) dan akan terlihat oleh siapa pun yang membuka source code halaman. Ini hanya penghalang ringan untuk mencegah akses tidak sengaja, **bukan keamanan tingkat produksi**. Jangan gunakan untuk data yang benar-benar sensitif tanpa mengganti sistem autentikasi dengan backend sungguhan.

## Batasan penting

- **Data tidak sinkron antar perangkat/browser.** Setiap perangkat yang membuka dasbor ini punya penyimpanan data sendiri-sendiri (`localStorage`). Data yang diinput di satu laptop tidak akan muncul di laptop atau HP lain.
- **Data bisa hilang** jika cache/data browser dibersihkan. Gunakan fitur **Konfigurasi → Ekspor Data (JSON)** secara berkala untuk membuat cadangan.
- Cocok untuk pemakaian oleh satu admin di satu perangkat. Untuk pemakaian multi-pengguna dengan data terpusat, diperlukan migrasi ke backend + database.

## Struktur repository

```
.
├── index.html   # seluruh aplikasi (HTML, CSS, JS dalam satu file)
└── README.md    # dokumen ini
```

## Cara mengaktifkan GitHub Pages

1. Buka repository ini di GitHub → **Settings** → **Pages**.
2. Pada bagian **Source**, pilih branch `main` dan folder `/ (root)`.
3. Klik **Save**. Tunggu 1–2 menit sampai GitHub selesai men-deploy.
4. Dasbor akan bisa diakses di `https://<username-anda>.github.io/<nama-repo>/`.

## Lisensi

Internal — silakan sesuaikan dengan kebutuhan PT. KJW.

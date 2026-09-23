# 🧱 Retro Stack

Game menyusun balok bergaya isometrik dengan tema retro/arcade (neon, scanline CRT, font pixel). Dibuat murni dengan **HTML, CSS, dan JavaScript** — tanpa library atau build tool apa pun.

## 📦 Isi Paket

```
index.html   # seluruh game (HTML + CSS + JS jadi satu file)
README.md          # file ini
```

## ⚙️ Cara Pemasangan

Tidak perlu instalasi apa pun. Pilih salah satu cara:

1. **Buka langsung**
   Klik dua kali file `index.html`, atau seret ke jendela browser (Chrome/Edge/Firefox/Safari terbaru).

2. **Jalankan lewat local server (opsional, disarankan untuk mobile testing)**
   ```bash
   # dari folder yang berisi index.html
   python3 -m http.server 8000
   ```
   Lalu buka `http://localhost:8000/index.html` di browser.

3. **Upload ke hosting statis**
   File ini bisa langsung diunggah ke GitHub Pages, Netlify, Vercel, atau hosting statis lain karena semuanya self-contained dalam satu file HTML.

> Butuh koneksi internet untuk memuat font *Press Start 2P* dari Google Fonts. Jika offline, game tetap berjalan tapi memakai font fallback monospace.

## 🎮 Cara Main

1. Balok pertama sudah terpasang di tengah sebagai fondasi.
2. Balok kedua bergerak bolak-balik secara otomatis.
3. **Klik / tap layar, atau tekan tombol Spasi** tepat saat balok berada di posisi yang sejajar dengan balok di bawahnya.
4. Bagian balok yang tidak sejajar (overhang) akan terpotong dan jatuh.
5. Setiap balok berhasil ditumpuk = skor +1, dan kecepatan gerak balok berikutnya sedikit meningkat.
6. Jika balok meleset total (tidak ada bagian yang tumpang tindih) → **Game Over**.
7. Tekan tombol **MAIN LAGI** untuk mengulang dari awal.

## 🕹️ Kontrol

| Aksi | Tombol |
|---|---|
| Taruh balok | Klik mouse / Tap layar / Tombol Spasi |
| Main ulang setelah kalah | Tombol "MAIN LAGI" di layar |

## 🏆 Skor

- **Score**: jumlah balok yang berhasil ditumpuk di sesi berjalan.
- **Best**: skor tertinggi, disimpan otomatis di browser (`localStorage`) sehingga tetap ada walau halaman ditutup — kecuali data situs/browser dibersihkan.

## 🛠️ Kustomisasi Singkat

Semua bisa diubah langsung di dalam `index.html`:

- **Warna tema**: ubah nilai di `:root { --bg1; --bg2; --accent; --accent2; --ink; }` dan array `PALETTE` di bagian JavaScript untuk warna balok.
- **Tinggi tiap balok**: ubah konstanta `BLOCK_H`.
- **Kecepatan awal & pertambahan kecepatan**: ubah `speed` dan rumus `speed = Math.min(7, 2.2 + score*0.12)`.
- **Lebar area gerak balok**: ubah variabel `range` (default `130`).

## 💻 Kompatibilitas

Bekerja di browser modern (Chrome, Edge, Firefox, Safari) versi terbaru, desktop maupun mobile. Tidak memerlukan Node.js, npm, atau dependensi eksternal apa pun selain koneksi ke Google Fonts (opsional).

## 📄 Lisensi

Bebas digunakan, dimodifikasi, dan dibagikan untuk keperluan pribadi maupun pembelajaran.

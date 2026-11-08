# 🐤 Pipit Terbang

Game ala Flappy Bird yang berjalan langsung di browser (HP maupun komputer). Tanpa instalasi, tanpa library, hanya satu file `index.html`.

## Cara bermain

- **HP / tablet:** ketuk layar untuk membuat pipit terbang.
- **Komputer:** tekan **Spasi** (atau `↑` / `W`), atau klik layar.
- Lewati celah di antara pilar kristal tanpa menabrak pilar atau tanah.
- Tekan **M** (atau tombol 🔊) untuk mematikan/menyalakan suara.
- Skor terbaik tersimpan otomatis di browser.

## Coba di komputer sendiri

Cukup klik dua kali `index.html`, game langsung terbuka di browser.

## Upload ke GitHub agar orang lain bisa main

Game ini cocok dipublikasikan lewat **GitHub Pages** (gratis). Setelah aktif, kamu mendapat link yang bisa dibagikan ke siapa saja.

### Cara 1: lewat website GitHub (paling mudah)

1. Login ke [github.com](https://github.com), klik **+** di kanan atas, lalu **New repository**.
2. Isi nama repo, misalnya `pipit-terbang`, pilih **Public**, lalu **Create repository**.
3. Klik **uploading an existing file**, tarik file `index.html` dan `README.md` ke halaman itu, lalu klik **Commit changes**.
4. Buka tab **Settings**, pilih **Pages** di menu kiri.
5. Pada **Build and deployment**, pilih **Source: Deploy from a branch**. Pilih branch `main` dan folder `/ (root)`, lalu **Save**.
6. Tunggu sekitar 1 menit, lalu muat ulang halaman Pages. Link game akan muncul di sana:

   ```
   https://USERNAME.github.io/pipit-terbang/
   ```

   Ganti `USERNAME` dengan username GitHub kamu.

### Cara 2: lewat terminal (git)

Buat repo kosong di GitHub dulu, lalu jalankan di folder berisi file game:

```bash
git init
git add index.html README.md
git commit -m "Game pertama: Pipit Terbang"
git branch -M main
git remote add origin https://github.com/USERNAME/pipit-terbang.git
git push -u origin main
```

Setelah itu aktifkan Pages seperti langkah 4–6 di atas.

### Update game

Setiap kali kamu mengubah `index.html` dan meng-upload ulang (atau `git push`), GitHub Pages akan memperbarui game otomatis dalam beberapa menit.

## Mengubah tingkat kesulitan

Buka `index.html`, cari bagian `Pengaturan` di awal script:

| Nilai | Fungsi |
|-------|--------|
| `GAP` | Lebar celah antar pilar (makin besar makin mudah) |
| `SPEED` | Kecepatan pilar bergerak |
| `SPACING` | Jarak antar pilar |
| `GRAVITY` / `FLAP_V` | Gaya tarik jatuh dan kekuatan lompatan |

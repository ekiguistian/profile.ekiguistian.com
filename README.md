# profile.ekiguistian.com

Situs portofolio statis Eki Guistian. Halaman disajikan dari file HTML, CSS, dan JavaScript; Tailwind sudah dikompilasi menjadi CSS statis untuk aaPanel.

## Struktur

- `index.html` — seluruh bagian halaman dan metadata SEO
- `assets/css/tailwind.input.css` — input Tailwind CSS 4.3.5
- `assets/css/tailwind.min.css` — utility Tailwind terkompilasi
- `assets/css/styles.css` — desain responsif, warna, tipografi, dan komponen
- `assets/js/main.js` — navigasi seluler dan tahun footer
- `assets/img/favicon.svg` — ikon situs

## Data profil

Bagian pendidikan, pengalaman kerja, dan usaha telah diisi dari informasi pemilik situs, termasuk peran Komisaris & Network Engineer di PT Synergi Antar Sahabat sejak 2024.

Proyek yang ditampilkan hanya **Mynet Billing**, sistem billing open source untuk pemain RT/RW Net dan ISP yang sedang dikembangkan. AI tetap ditandai sebagai area eksplorasi, bukan klaim pengalaman atau keahlian.

Ikon memakai Font Awesome Free 7.3.1 melalui [jsDelivr](https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@7.3.1/css/fontawesome.min.css). Tailwind Play CDN tidak dipakai di produksi; utility CSS dikompilasi dan disimpan lokal agar halaman aaPanel tidak perlu menjalankan JavaScript Tailwind di browser.

## Menjalankan lokal

Buka `index.html` melalui server statis lokal. Jika mengubah utility class Tailwind, unduh executable Windows x64 dari [release Tailwind CLI v4.3.5](https://github.com/tailwindlabs/tailwindcss/releases/tag/v4.3.5), lalu kompilasi ulang:

```powershell
tailwindcss-windows-x64.exe -i assets/css/tailwind.input.css -o assets/css/tailwind.min.css --minify
```

File `tailwind.min.css` sudah tersedia di repository, sehingga server produksi hanya perlu menyajikan file statis.

## Deploy melalui aaPanel

Situs ini berupa file statis dan dilayani melalui aaPanel. Pull isi repository ke document root domain `profile.ekiguistian.com`, dengan `index.html` berada di root. Server produksi tidak memerlukan Node.js atau runtime PHP. Atur DNS domain dan sertifikat HTTPS dari aaPanel sesuai konfigurasi server.

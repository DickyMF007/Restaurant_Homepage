# 📁 Panduan Menambahkan Gambar

Folder ini digunakan untuk menyimpan semua gambar yang digunakan di website.

## 📂 Struktur Folder yang Disarankan

```
assets/images/
├── hero-bg.jpg              # Background hero section
├── about-bg.jpg             # Background about section  
├── features-bg.jpg          # Background features section
├── about-restaurant.jpg     # Gambar utama di about section
├── logo.png                 # Logo restoran
├── icons/                   # Folder untuk icons
│   ├── menu-icon.svg
│   ├── chef-icon.svg
│   └── ...
└── menu/                    # Folder untuk gambar menu
    ├── salad-segar.jpg
    ├── sup-krim-jamur.jpg
    └── ...
```

## 🖼️ Ukuran Gambar yang Disarankan

### Background Images
- **Hero Background**: 1920x1080px (16:9 ratio)
- **About Background**: 1920x1080px
- **Features Background**: 1920x1080px

### Content Images
- **About Restaurant Image**: 800x600px (4:3 ratio)
- **Menu Images**: 600x400px (3:2 ratio)
- **Logo**: Sesuai kebutuhan (disarankan tinggi 50-100px)

### Icons
- **SVG Icons**: Scalable (disarankan)
- **PNG Icons**: 64x64px atau 128x128px

## 📝 Format File

### Gambar Foto
- **JPG**: Untuk foto dengan banyak warna (ukuran lebih kecil)
- **PNG**: Untuk gambar dengan transparansi
- **WebP**: Format modern dengan kompresi lebih baik (disarankan)

### Icons
- **SVG**: Format terbaik untuk icons (scalable, ukuran kecil)
- **PNG**: Alternatif jika SVG tidak tersedia

## 🎯 Cara Menambahkan Gambar

### 1. Background Hero

1. Letakkan gambar di folder ini dengan nama `hero-bg.jpg`
2. Atau edit CSS variable di `style.css`:
   ```css
   --hero-bg-image: url('assets/images/nama-file-anda.jpg');
   ```

### 2. Gambar Menu

1. Letakkan gambar menu di folder ini
2. Edit `main.js`, update property `image` di array `menuData`:
   ```javascript
   {
       name: 'Nama Menu',
       image: 'assets/images/nama-gambar.jpg'
   }
   ```

### 3. Gambar About Section

1. Letakkan gambar di folder ini
2. Edit `index.html`, uncomment dan update:
   ```html
   <img src="assets/images/about-restaurant.jpg" alt="About Restaurant">
   ```

### 4. Logo

1. Letakkan logo di folder ini
2. Edit `index.html`:
   ```html
   <img src="assets/images/logo.png" alt="Logo">
   ```

## ⚡ Optimasi Gambar

Sebelum upload, optimasi gambar Anda:

### Tools Online
- [TinyPNG](https://tinypng.com/) - Kompres PNG/JPG
- [Squoosh](https://squoosh.app/) - Konversi ke WebP
- [ImageOptim](https://imageoptim.com/) - Desktop tool

### Tips Optimasi
1. **Resize** gambar ke ukuran yang diperlukan
2. **Kompres** gambar untuk mengurangi ukuran file
3. **Konversi ke WebP** untuk ukuran lebih kecil
4. **Gunakan lazy loading** untuk performa lebih baik

## 🔍 Troubleshooting

### Gambar Tidak Muncul
- Pastikan path benar (relative dari `index.html`)
- Cek nama file (case-sensitive)
- Pastikan file ada di folder yang benar
- Cek console browser untuk error

### Gambar Terlalu Besar
- Kompres gambar menggunakan tools di atas
- Resize ke ukuran yang sesuai
- Konversi ke format WebP

### Gambar Terlalu Kecil/Buram
- Gunakan gambar dengan resolusi lebih tinggi
- Pastikan gambar tidak di-stretch
- Gunakan format SVG untuk icons

## 📚 Resources

- [Unsplash](https://unsplash.com/) - Free high-quality photos
- [Pexels](https://www.pexels.com/) - Free stock photos
- [Flaticon](https://www.flaticon.com/) - Free icons
- [Font Awesome](https://fontawesome.com/) - Icon library

---

**Catatan**: Pastikan semua gambar yang digunakan memiliki lisensi yang sesuai untuk penggunaan komersial.


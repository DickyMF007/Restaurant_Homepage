# 📸 Folder Images - Panduan Penggunaan

Folder ini digunakan untuk menyimpan semua gambar menu restoran.

## 📁 Struktur File

Semua gambar menu harus ditempatkan di folder ini dengan format nama yang konsisten.

## 📝 Format Nama File

Gunakan format berikut untuk nama file gambar:

- **Format**: `nama-menu.jpg` atau `nama-menu.png`
- **Gunakan lowercase** (huruf kecil)
- **Gunakan dash/hyphen (-)** untuk memisahkan kata
- **Hindari spasi** dan karakter khusus

### Contoh Nama File yang Benar:
- ✅ `salad-segar.jpg`
- ✅ `sup-krim-jamur.jpg`
- ✅ `steak-sirloin.jpg`
- ✅ `pasta-carbonara.jpg`
- ✅ `tiramisu.jpg`

### Contoh Nama File yang Salah:
- ❌ `Salad Segar.jpg` (ada spasi dan huruf besar)
- ❌ `sup_krim_jamur.jpg` (menggunakan underscore)
- ❌ `Steak-Sirloin.jpg` (huruf besar)
- ❌ `pasta carbonara.jpg` (ada spasi)

## 🖼️ Format Gambar yang Disarankan

### Format File:
- **JPG/JPEG**: Untuk foto makanan (disarankan)
- **PNG**: Untuk gambar dengan transparansi
- **WebP**: Untuk optimasi (opsional, browser support modern)

### Spesifikasi Gambar:
- **Ukuran**: Disarankan 800x600px atau 1200x800px
- **Rasio**: 4:3 atau 16:9
- **Ukuran File**: Maksimal 500KB per gambar (untuk performa)
- **Kualitas**: High quality tapi dioptimasi untuk web

## 🔗 Menghubungkan Gambar ke Menu

Setelah menambahkan gambar ke folder ini, update file `main.js` di bagian `menuData`:

```javascript
{
    name: 'Nama Menu',
    price: 'Rp 100.000',
    description: 'Deskripsi menu',
    category: 'main',
    image: 'assets/images/nama-file-gambar.jpg' // Path relatif dari index.html
}
```

### Path yang Benar:
- ✅ `assets/images/nama-menu.jpg` (jika dari root project)
- ✅ `../images/nama-menu.jpg` (jika dari folder lain)

## 📋 Daftar Gambar yang Diperlukan

Berdasarkan menu yang ada, berikut adalah daftar gambar yang perlu ditambahkan:

### Hidangan Pembuka (Appetizer):
- [ ] `salad-segar.jpg`
- [ ] `sup-krim-jamur.jpg`
- [ ] `bruschetta.jpg`

### Hidangan Utama (Main):
- [ ] `steak-sirloin.jpg`
- [ ] `salmon-panggang.jpg`
- [ ] `pasta-carbonara.jpg`
- [ ] `risotto-jamur.jpg`
- [ ] `burger-premium.jpg`
- [ ] `pizza-margherita.jpg`

### Pencuci Mulut (Dessert):
- [ ] `tiramisu.jpg`
- [ ] `cheesecake.jpg`
- [ ] `chocolate-lava.jpg`
- [ ] `ice-cream-sundae.jpg`

### Minuman (Drink):
- [ ] `fresh-orange-juice.jpg`
- [ ] `cappuccino.jpg`
- [ ] `lemonade.jpg`
- [ ] `smoothie-berry.jpg`

## 🛠️ Tips Optimasi Gambar

### Sebelum Upload:
1. **Resize**: Sesuaikan ukuran gambar (tidak perlu terlalu besar)
2. **Compress**: Gunakan tool seperti TinyPNG atau ImageOptim
3. **Format**: Pilih format yang tepat (JPG untuk foto, PNG untuk transparansi)

### Tools yang Disarankan:
- **Online**: TinyPNG, Squoosh, ImageOptim
- **Desktop**: GIMP, Photoshop, ImageOptim (Mac)
- **Command Line**: ImageMagick, jpegoptim

## 🔄 Mengganti Gambar

Untuk mengganti gambar menu:

1. **Ganti file gambar** dengan nama yang sama di folder ini
2. **Atau** ubah nama file dan update path di `main.js`
3. **Clear browser cache** jika gambar tidak berubah (Ctrl+F5 atau Cmd+Shift+R)

## ⚠️ Catatan Penting

- **Fallback**: Jika gambar tidak ditemukan, akan muncul placeholder SVG otomatis
- **Loading**: Gambar menggunakan `loading="lazy"` untuk performa yang lebih baik
- **Alt Text**: Alt text otomatis menggunakan nama menu
- **Error Handling**: Jika gambar gagal dimuat, akan muncul placeholder

## 📚 Sumber Gambar Gratis

Jika Anda membutuhkan gambar makanan gratis, berikut beberapa sumber:

- **Unsplash**: https://unsplash.com/s/photos/food
- **Pexels**: https://www.pexels.com/search/food/
- **Pixabay**: https://pixabay.com/images/search/food/
- **Foodiesfeed**: https://www.foodiesfeed.com/

**Catatan**: Pastikan untuk memeriksa lisensi gambar sebelum digunakan untuk keperluan komersial.

---

**Last Updated**: 2024


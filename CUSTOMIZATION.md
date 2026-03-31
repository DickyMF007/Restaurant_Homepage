# 🎨 Panduan Kustomisasi - Restaurant Homepage

Panduan lengkap untuk mengganti gambar, icon, warna, dan komponen lainnya dengan mudah.

## 📋 Daftar Isi

- [Mengganti Background Images](#mengganti-background-images)
- [Mengganti Icons](#mengganti-icons)
- [Mengganti Warna Theme](#mengganti-warna-theme)
- [Mengganti Logo](#mengganti-logo)
- [Mengganti Gambar Menu](#mengganti-gambar-menu)
- [Mengganti Gambar About Section](#mengganti-gambar-about-section)

---

## 🖼️ Mengganti Background Images

### Hero Background

**Metode 1: Menggunakan CSS Variable (Recommended)**

Edit file `assets/css/style.css`, cari bagian `:root` dan ubah:

```css
:root {
    --hero-bg-image: url('assets/images/hero-bg.jpg');
}
```

**Metode 2: Menggunakan Data Attribute di HTML**

Edit file `index.html`, pada section hero:

```html
<section id="home" class="hero" data-bg-image="assets/images/hero-bg-custom.jpg">
```

**Langkah-langkah:**
1. Letakkan gambar Anda di folder `assets/images/`
2. Ganti nama file sesuai dengan path yang Anda set
3. Format gambar yang disarankan: JPG, PNG, atau WebP
4. Ukuran optimal: 1920x1080px atau lebih besar

### About Section Background

Edit CSS variable di `style.css`:

```css
:root {
    --about-bg-image: url('assets/images/about-bg.jpg');
}
```

### Features Section Background

Edit CSS variable di `style.css`:

```css
:root {
    --features-bg-image: url('assets/images/features-bg.jpg');
}
```

---

## 🎯 Mengganti Icons

### Menggunakan CSS Variables (Recommended)

Semua icon dapat diganti melalui CSS variables di `style.css`:

```css
:root {
    --icon-logo: '🍽️';           /* Logo icon */
    --icon-menu: '🍴';             /* Menu feature icon */
    --icon-chef: '👨‍🍳';          /* Chef feature icon */
    --icon-organic: '🌿';          /* Organic feature icon */
    --icon-service: '⭐';           /* Service feature icon */
    --icon-location: '📍';          /* Location contact icon */
    --icon-phone: '📞';            /* Phone contact icon */
    --icon-email: '✉️';            /* Email contact icon */
    --icon-time: '🕒';             /* Time contact icon */
    --icon-facebook: '📘';         /* Facebook social icon */
    --icon-instagram: '📷';        /* Instagram social icon */
    --icon-twitter: '🐦';          /* Twitter social icon */
}
```

### Menggunakan Emoji

Ganti langsung di HTML dengan emoji yang diinginkan:

```html
<div class="feature-icon" data-icon="menu">🍴</div>
```

### Menggunakan Image/SVG

**Metode 1: Menggunakan CSS**

Tambahkan di `style.css`:

```css
.feature-icon[data-icon="menu"] {
    background-image: url('assets/images/icons/menu-icon.svg');
    background-size: contain;
    background-repeat: no-repeat;
    background-position: center;
    width: 64px;
    height: 64px;
    font-size: 0; /* Hide emoji */
}
```

**Metode 2: Menggunakan HTML**

Ganti di `index.html`:

```html
<div class="feature-icon">
    <img src="assets/images/icons/menu-icon.svg" alt="Menu">
</div>
```

---

## 🎨 Mengganti Warna Theme

Edit CSS variables di `style.css` bagian `:root`:

```css
:root {
    /* Primary Colors - Warna utama */
    --primary-color: #ff6b6b;        /* Merah coral */
    --secondary-color: #4ecdc4;      /* Turquoise */
    --accent-color: #ffe66d;         /* Kuning cerah */
    
    /* Neutral Colors */
    --dark-color: #2c2c2c;           /* Hitam */
    --light-color: #ffffff;          /* Putih */
    --bg-light: #f8f9fa;             /* Background terang */
    --text-color: #2d3436;           /* Warna teks utama */
    --text-light: #636e72;           /* Warna teks sekunder */
    
    /* Gradients */
    --gradient-primary: linear-gradient(135deg, #ff6b6b 0%, #ee5a6f 100%);
    --gradient-secondary: linear-gradient(135deg, #4ecdc4 0%, #44a08d 100%);
    --gradient-hero: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
    --gradient-accent: linear-gradient(135deg, #ffe66d 0%, #ffd93d 100%);
}
```

### Contoh Skema Warna Lainnya

**Skema Hijau Segar:**
```css
--primary-color: #2ecc71;
--secondary-color: #27ae60;
--accent-color: #f39c12;
```

**Skema Biru Modern:**
```css
--primary-color: #3498db;
--secondary-color: #2980b9;
--accent-color: #e74c3c;
```

**Skema Ungu Elegan:**
```css
--primary-color: #9b59b6;
--secondary-color: #8e44ad;
--accent-color: #f39c12;
```

---

## 🏷️ Mengganti Logo

### Menggunakan Text/Emoji

Edit di `index.html`:

```html
<div class="logo">
    <h2 data-icon="logo">🍽️ Bistro</h2>
</div>
```

Ganti `🍽️ Bistro` dengan logo text Anda.

### Menggunakan Image

Edit di `index.html`:

```html
<div class="logo">
    <img src="assets/images/logo.png" alt="Restaurant Logo" style="height: 50px;">
</div>
```

Atau edit CSS untuk styling lebih lanjut:

```css
.logo img {
    height: 50px;
    width: auto;
}
```

---

## 🍽️ Mengganti Gambar Menu

Gambar menu dikelola melalui JavaScript di `assets/js/main.js`.

Edit array `menuData`:

```javascript
const menuData = [
    {
        name: 'Salad Segar',
        price: 'Rp 45.000',
        description: 'Campuran sayuran segar dengan dressing khusus',
        category: 'appetizer',
        image: 'assets/images/salad-segar.jpg'  // Ganti path ini
    },
    // ... item lainnya
];
```

**Langkah-langkah:**
1. Letakkan gambar menu di folder `assets/images/`
2. Update property `image` dengan path yang benar
3. Format yang disarankan: JPG, PNG, atau WebP
4. Ukuran optimal: 600x400px atau lebih besar

---

## 📸 Mengganti Gambar About Section

**Metode 1: Menggunakan HTML Image**

Edit di `index.html`, uncomment dan ganti path:

```html
<div class="about-image">
    <img src="assets/images/about-restaurant.jpg" alt="About Restaurant">
    <!-- Hapus atau comment div image-placeholder jika menggunakan gambar -->
    <!-- <div class="image-placeholder">
        <span>🍽️</span>
    </div> -->
</div>
```

**Metode 2: Menggunakan CSS Background**

Edit CSS variable:

```css
:root {
    --about-bg-image: url('assets/images/about-restaurant.jpg');
}
```

Kemudian gambar akan muncul sebagai background pada placeholder.

---

## 🎭 Tips Kustomisasi

### 1. Konsistensi Warna
- Gunakan maksimal 3-4 warna utama
- Pastikan kontras yang cukup untuk readability
- Test di berbagai perangkat dan browser

### 2. Optimasi Gambar
- Gunakan format WebP untuk ukuran lebih kecil
- Kompres gambar sebelum upload
- Gunakan lazy loading untuk performa lebih baik

### 3. Ukuran Gambar
- **Hero Background**: 1920x1080px atau lebih besar
- **Menu Images**: 600x400px
- **About Image**: 800x600px
- **Icons**: 64x64px atau SVG

### 4. Format File
- **Gambar**: JPG (untuk foto), PNG (untuk transparansi), WebP (optimal)
- **Icons**: SVG (scalable) atau PNG
- **Logo**: SVG atau PNG dengan transparansi

---

## 🔧 Troubleshooting

### Gambar Tidak Muncul
1. Pastikan path gambar benar (relative dari `index.html`)
2. Cek nama file (case-sensitive di beberapa server)
3. Pastikan file ada di folder yang benar
4. Cek console browser untuk error

### Icon Tidak Berubah
1. Pastikan CSS variable sudah diupdate di `:root`
2. Clear browser cache (Ctrl+F5)
3. Cek apakah ada CSS lain yang override

### Warna Tidak Berubah
1. Pastikan CSS variable diupdate di bagian `:root`
2. Pastikan tidak ada inline style yang override
3. Clear browser cache

---

## 📝 Checklist Kustomisasi

- [ ] Background hero sudah diganti
- [ ] Logo sudah diganti
- [ ] Warna theme sudah disesuaikan
- [ ] Icons sudah diganti (jika perlu)
- [ ] Gambar menu sudah ditambahkan
- [ ] Gambar about section sudah ditambahkan
- [ ] Semua gambar sudah dioptimasi
- [ ] Test di berbagai browser
- [ ] Test di berbagai ukuran layar

---

**Catatan**: Setelah melakukan perubahan, selalu test website di berbagai browser dan perangkat untuk memastikan tampilan tetap konsisten dan menarik.


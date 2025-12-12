# 🍽️ Restaurant Homepage

Homepage restoran modern dan responsif yang dibangun dengan HTML, CSS, dan JavaScript vanilla. Website ini menampilkan menu restoran, informasi tentang restoran, testimoni pelanggan, dan formulir kontak.

## 📋 Daftar Isi

- [Fitur](#fitur)
- [Teknologi yang Digunakan](#teknologi-yang-digunakan)
- [Struktur Proyek](#struktur-proyek)
- [Instalasi](#instalasi)
- [Penggunaan](#penggunaan)
- [Struktur File](#struktur-file)
- [Kustomisasi](#kustomisasi)
- [Browser Support](#browser-support)
- [Lisensi](#lisensi)

## ✨ Fitur

### 🎨 Desain & UI/UX
- **Desain Modern**: Interface yang bersih dan modern dengan skema warna yang menarik
- **Responsif**: Fully responsive untuk semua perangkat (desktop, tablet, mobile)
- **Animasi**: Smooth animations dan transitions untuk pengalaman yang lebih baik
- **Typography**: Menggunakan Google Fonts (Playfair Display & Poppins)

### 🧭 Navigasi
- **Fixed Navigation Bar**: Navigation bar yang tetap terlihat saat scroll
- **Smooth Scroll**: Navigasi halus antar section
- **Mobile Menu**: Hamburger menu untuk perangkat mobile
- **Active States**: Indikator visual untuk link aktif

### 📱 Sections

1. **Hero Section**
   - Background gradient yang menarik
   - Call-to-action buttons
   - Scroll indicator

2. **Features Section**
   - 4 fitur utama restoran
   - Card design dengan hover effects

3. **Menu Section**
   - Filter menu berdasarkan kategori
   - 17+ item menu dengan harga
   - Grid layout responsif
   - Kategori: Hidangan Pembuka, Hidangan Utama, Pencuci Mulut, Minuman

4. **About Section**
   - Informasi tentang restoran
   - Statistik (Tahun Pengalaman, Menu Pilihan, Pelanggan Puas)
   - Two-column layout

5. **Testimonials Section**
   - Ulasan dari pelanggan
   - Rating stars
   - Card design dengan hover effects

6. **Contact Section**
   - Informasi kontak (alamat, telepon, email, jam operasional)
   - Form kontak yang fungsional
   - Validasi form

7. **Footer**
   - Informasi restoran
   - Quick links
   - Social media links

### ⚡ Interaktivitas
- **Menu Filtering**: Filter menu berdasarkan kategori
- **Form Handling**: Form kontak dengan validasi
- **Scroll Animations**: Animasi saat scroll menggunakan Intersection Observer
- **Mobile Navigation**: Toggle menu untuk mobile devices

## 🛠️ Teknologi yang Digunakan

- **HTML5**: Struktur semantic dan modern
- **CSS3**: 
  - CSS Grid & Flexbox untuk layout
  - CSS Variables untuk theming
  - Media queries untuk responsivitas
  - Animations & Transitions
- **JavaScript (Vanilla)**:
  - DOM Manipulation
  - Event Listeners
  - Intersection Observer API
  - Local data storage untuk menu items

## 📁 Struktur Proyek

```
Restaurant_Homepage/
│
├── frontend-only/
│   ├── index.html              # File HTML utama
│   │
│   └── assets/
│       ├── css/
│       │   └── style.css       # Stylesheet utama
│       │
│       ├── js/
│       │   └── main.js         # JavaScript utama
│       │
│       └── images/              # Folder untuk gambar (kosong)
│
└── README.md                    # Dokumentasi proyek
```

## 🚀 Instalasi

### Prasyarat
- Web browser modern (Chrome, Firefox, Safari, Edge)
- Web server (opsional, untuk development)

### Langkah Instalasi

1. **Clone atau Download Repository**
   ```bash
   git clone https://github.com/username/Restaurant_Homepage.git
   cd Restaurant_Homepage
   ```

2. **Buka di Browser**
   - Buka file `frontend-only/index.html` langsung di browser, atau
   - Gunakan web server lokal untuk development

### Menggunakan Web Server Lokal (Opsional)

**Python:**
```bash
cd frontend-only
python -m http.server 8000
```
Kemudian buka `http://localhost:8000` di browser

**Node.js (http-server):**
```bash
npm install -g http-server
cd frontend-only
http-server
```

**VS Code Live Server:**
- Install extension "Live Server"
- Klik kanan pada `index.html` → "Open with Live Server"

## 📖 Penggunaan

### Navigasi
- Klik pada menu navigation untuk scroll ke section yang diinginkan
- Gunakan hamburger menu (☰) di mobile untuk membuka/menutup menu

### Menu Filtering
1. Klik pada tab kategori di section Menu
2. Menu akan otomatis terfilter berdasarkan kategori yang dipilih
3. Klik "Semua" untuk menampilkan semua menu

### Form Kontak
1. Isi form dengan informasi yang diperlukan
2. Klik "Kirim Pesan" untuk mengirim
3. Form akan menampilkan alert konfirmasi (dapat dikustomisasi untuk mengirim ke server)

## 📄 Struktur File

### index.html
File HTML utama yang berisi struktur website dengan sections:
- Navigation bar
- Hero section
- Features section
- Menu section
- About section
- Testimonials section
- Contact section
- Footer

### assets/css/style.css
Stylesheet utama yang berisi:
- CSS Variables untuk theming
- Reset & Base styles
- Navigation styles
- Hero section styles
- Features section styles
- Menu section styles
- About section styles
- Testimonials section styles
- Contact section styles
- Footer styles
- Animations & Keyframes
- Media queries untuk responsivitas

### assets/js/main.js
JavaScript utama yang berisi:
- Mobile navigation toggle
- Smooth scroll functionality
- Menu data dan rendering
- Menu filtering logic
- Contact form handler
- Scroll animations dengan Intersection Observer

## 🎨 Kustomisasi

### Mengubah Warna Theme

Edit CSS variables di `style.css`:

```css
:root {
    --primary-color: #d4a574;      /* Warna utama (gold) */
    --secondary-color: #8b4513;    /* Warna sekunder (brown) */
    --dark-color: #2c2c2c;         /* Warna gelap */
    --light-color: #f8f8f8;        /* Warna terang */
    --text-color: #333;            /* Warna teks */
}
```

### Menambah/Mengubah Menu Items

Edit array `menuData` di `main.js`:

```javascript
const menuData = [
    {
        name: 'Nama Menu',
        price: 'Rp 100.000',
        description: 'Deskripsi menu',
        category: 'main',  // 'appetizer', 'main', 'dessert', 'drink'
        emoji: '🍽️'
    },
    // ... tambahkan item lainnya
];
```

### Mengubah Konten

1. **Nama Restoran**: Edit di `index.html` (logo dan hero title)
2. **Informasi Kontak**: Edit di section Contact di `index.html`
3. **About Section**: Edit teks di section About di `index.html`
4. **Testimonials**: Edit card testimonial di `index.html`

### Menambah Gambar

1. Tambahkan gambar ke folder `assets/images/`
2. Update HTML untuk menggunakan gambar:
   ```html
   <img src="assets/images/nama-gambar.jpg" alt="Deskripsi">
   ```
3. Atau update CSS untuk menggunakan gambar sebagai background

### Mengubah Font

Edit link Google Fonts di `index.html`:
```html
<link href="https://fonts.googleapis.com/css2?family=FontName&display=swap" rel="stylesheet">
```

Kemudian update font-family di CSS:
```css
body {
    font-family: 'FontName', sans-serif;
}
```

## 🌐 Browser Support

Website ini kompatibel dengan:
- ✅ Chrome (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Edge (latest)
- ✅ Opera (latest)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 📝 Catatan Pengembangan

### Fitur yang Dapat Ditambahkan
- [ ] Integrasi dengan backend untuk form kontak
- [ ] Database untuk menu items
- [ ] Sistem reservasi online
- [ ] Galeri foto
- [ ] Blog/News section
- [ ] Multi-language support
- [ ] Dark mode toggle
- [ ] Search functionality untuk menu
- [ ] Shopping cart untuk online ordering
- [ ] Integration dengan Google Maps untuk lokasi

### Optimasi yang Dapat Dilakukan
- [ ] Lazy loading untuk images
- [ ] Minify CSS dan JavaScript untuk production
- [ ] Optimize images (WebP format)
- [ ] Add service worker untuk PWA
- [ ] SEO optimization (meta tags, structured data)

## 🤝 Kontribusi

Kontribusi sangat diterima! Untuk berkontribusi:

1. Fork repository
2. Buat feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit perubahan (`git commit -m 'Add some AmazingFeature'`)
4. Push ke branch (`git push origin feature/AmazingFeature`)
5. Buat Pull Request

## 📄 Lisensi

Proyek ini menggunakan lisensi MIT. Lihat file `LICENSE` untuk detail lebih lanjut.

## 👤 Author

Dibuat dengan ❤️ untuk Restaurant Homepage Project

## 🙏 Acknowledgments

- Google Fonts untuk typography
- Inspirasi dari berbagai restaurant websites
- Community untuk feedback dan suggestions

---

**Catatan**: Website ini adalah frontend-only dan tidak memerlukan backend untuk berfungsi. Semua data menu disimpan di JavaScript file. Untuk production, disarankan untuk mengintegrasikan dengan backend API.


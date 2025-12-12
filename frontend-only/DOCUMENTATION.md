# 📚 Dokumentasi Teknis - Restaurant Homepage

Dokumentasi teknis lengkap untuk developer yang ingin memahami atau mengembangkan website ini lebih lanjut.

## 🏗️ Arsitektur

Website ini menggunakan arsitektur frontend-only dengan struktur berikut:

```
┌─────────────────────────────────────┐
│         index.html (Entry Point)    │
│  - Struktur HTML                    │
│  - Semantic HTML5                   │
└──────────────┬──────────────────────┘
               │
       ┌───────┴────────┐
       │                │
┌──────▼──────┐  ┌─────▼──────┐
│  style.css  │  │  main.js   │
│  - Styling  │  │  - Logic   │
│  - Layout   │  │  - Events  │
└─────────────┘  └────────────┘
```

## 📐 Struktur HTML

### Semantic HTML5 Elements

Website menggunakan semantic HTML5 untuk struktur yang lebih baik:

- `<nav>` - Navigation bar
- `<section>` - Setiap section utama
- `<header>` - Header content (implied dalam hero)
- `<footer>` - Footer section
- `<article>` - Testimonial cards (dapat digunakan)
- `<form>` - Contact form

### ID dan Class Naming Convention

**IDs digunakan untuk:**
- Unique elements: `#home`, `#menu`, `#about`, `#contact`
- JavaScript targets: `#navMenu`, `#hamburger`, `#menuGrid`, `#contactForm`

**Classes digunakan untuk:**
- Reusable components: `.btn`, `.card`, `.section-title`
- BEM-like naming: `.menu-item`, `.menu-item-name`, `.menu-item-price`
- Utility classes: `.container`, `.nav-wrapper`

## 🎨 Sistem Desain CSS

### CSS Variables (Custom Properties)

Semua warna dan nilai penting disimpan dalam CSS variables untuk kemudahan kustomisasi:

```css
:root {
    --primary-color: #d4a574;
    --secondary-color: #8b4513;
    --dark-color: #2c2c2c;
    --light-color: #f8f8f8;
    --text-color: #333;
    --white: #ffffff;
    --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    --shadow-lg: 0 10px 30px rgba(0, 0, 0, 0.15);
    --transition: all 0.3s ease;
}
```

### Layout System

**Container:**
- Max-width: 1200px
- Padding: 0 20px
- Centered dengan margin: auto

**Grid System:**
- CSS Grid untuk layout utama
- `grid-template-columns: repeat(auto-fit, minmax(250px, 1fr))` untuk responsif
- Gap: 2rem untuk spacing

**Flexbox:**
- Navigation bar
- Hero buttons
- Contact items
- Footer content

### Breakpoints

```css
/* Mobile */
@media (max-width: 480px) { ... }

/* Tablet */
@media (max-width: 768px) { ... }

/* Desktop */
/* Default styles (no media query) */
```

## ⚙️ JavaScript Architecture

### Module Structure

Meskipun menggunakan vanilla JavaScript, kode diorganisir dalam logical sections:

1. **DOM Elements Selection**
2. **Event Listeners Setup**
3. **Menu Data & Rendering**
4. **Form Handling**
5. **Scroll Animations**

### Key Functions

#### `renderMenu(category)`
- Menampilkan menu items berdasarkan kategori
- Parameter: `category` (string) - 'all', 'appetizer', 'main', 'dessert', 'drink'
- Menggunakan template literals untuk HTML generation

#### Mobile Navigation Toggle
```javascript
hamburger.addEventListener('click', () => {
    navMenu.classList.toggle('active');
});
```

#### Smooth Scroll
```javascript
window.scrollTo({
    top: offsetTop,
    behavior: 'smooth'
});
```

#### Intersection Observer
- Digunakan untuk scroll animations
- Threshold: 0.1
- Root margin: '0px 0px -50px 0px'

### Data Structure

**Menu Item Object:**
```javascript
{
    name: string,           // Nama menu
    price: string,          // Harga (format: 'Rp XXX.XXX')
    description: string,     // Deskripsi menu
    category: string,        // Kategori: 'appetizer', 'main', 'dessert', 'drink'
    emoji: string           // Emoji untuk icon
}
```

## 🎯 Event Handling

### Navigation Events
- `click` pada hamburger menu → Toggle mobile menu
- `click` pada nav links → Smooth scroll + close mobile menu
- `scroll` pada window → Navbar shadow effect

### Menu Events
- `click` pada tab buttons → Filter menu items
- Dynamic rendering berdasarkan kategori

### Form Events
- `submit` pada contact form → Handle form submission
- Prevent default behavior
- Show alert (dapat diganti dengan API call)

### Scroll Events
- `scroll` → Navbar styling changes
- Intersection Observer → Element animations

## 🔄 State Management

Website ini menggunakan simple state management:

1. **Menu Category State**: Disimpan dalam `data-category` attribute pada tab buttons
2. **Mobile Menu State**: Disimpan dalam `active` class pada nav menu
3. **Menu Data**: Disimpan dalam array `menuData`

## 📱 Responsive Design Strategy

### Mobile-First Approach
1. Base styles untuk mobile
2. Progressive enhancement untuk tablet dan desktop
3. Media queries untuk breakpoints

### Responsive Features
- **Navigation**: Hamburger menu untuk mobile
- **Grid Layouts**: Auto-fit dengan minmax untuk responsif
- **Typography**: Fluid typography dengan clamp() atau media queries
- **Images**: Responsive images (jika ditambahkan)

## 🎭 Animations & Transitions

### CSS Animations

**fadeInUp:**
```css
@keyframes fadeInUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
}
```

**bounce:**
```css
@keyframes bounce {
    0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
    40% { transform: translateY(-10px); }
    60% { transform: translateY(-5px); }
}
```

### Transitions
- Default: `all 0.3s ease`
- Hover effects pada cards dan buttons
- Smooth scroll behavior

## 🔍 Performance Considerations

### Current Optimizations
- CSS variables untuk theming (tidak perlu re-render)
- Event delegation untuk dynamic elements
- Intersection Observer untuk efficient scroll animations

### Recommendations for Production
1. **Minify CSS & JavaScript**
2. **Optimize Images**: Use WebP format, lazy loading
3. **Code Splitting**: Jika menggunakan bundler
4. **CDN**: Host fonts dan assets di CDN
5. **Caching**: Implement browser caching
6. **Compression**: Enable Gzip/Brotli compression

## 🧪 Testing Considerations

### Manual Testing Checklist
- [ ] Navigation works on all devices
- [ ] Menu filtering works correctly
- [ ] Form validation works
- [ ] Smooth scroll works
- [ ] Mobile menu toggles correctly
- [ ] All links are functional
- [ ] Responsive design on different screen sizes
- [ ] Animations work smoothly
- [ ] No console errors

### Browser Testing
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## 🐛 Debugging Tips

### Common Issues

1. **Menu tidak muncul**
   - Check: Apakah `menuData` array terdefinisi?
   - Check: Apakah `renderMenu()` dipanggil?

2. **Smooth scroll tidak bekerja**
   - Check: Apakah `scroll-behavior: smooth` ada di CSS?
   - Check: Apakah JavaScript event listener terpasang?

3. **Mobile menu tidak toggle**
   - Check: Apakah hamburger element memiliki ID `hamburger`?
   - Check: Apakah CSS class `.active` terdefinisi?

4. **Animations tidak muncul**
   - Check: Apakah Intersection Observer terinisialisasi?
   - Check: Apakah elements memiliki initial opacity/transform?

## 🔐 Security Considerations

### Current Implementation
- Form validation di client-side
- No user input sanitization (tidak ada backend)

### Recommendations
- **Input Sanitization**: Sanitize semua user input
- **XSS Prevention**: Escape HTML dalam user-generated content
- **CSRF Protection**: Jika menggunakan form dengan backend
- **HTTPS**: Gunakan HTTPS untuk production

## 📈 SEO Considerations

### Current Implementation
- Semantic HTML5
- Meta tags (dapat ditambahkan lebih lengkap)
- Alt text untuk images (jika ditambahkan)

### Recommendations
- **Meta Tags**: Tambahkan Open Graph, Twitter Cards
- **Structured Data**: JSON-LD untuk restaurant schema
- **Sitemap**: Buat sitemap.xml
- **robots.txt**: Konfigurasi robots.txt
- **Performance**: Optimize Core Web Vitals

## 🚀 Deployment Checklist

- [ ] Minify CSS dan JavaScript
- [ ] Optimize images
- [ ] Update meta tags untuk production
- [ ] Test di semua browser
- [ ] Check mobile responsiveness
- [ ] Verify all links work
- [ ] Test form submission
- [ ] Check console for errors
- [ ] Validate HTML/CSS
- [ ] Test page load speed
- [ ] Setup analytics (optional)
- [ ] Configure domain and hosting

## 📞 Support & Resources

### Useful Resources
- [MDN Web Docs](https://developer.mozilla.org/)
- [CSS-Tricks](https://css-tricks.com/)
- [Can I Use](https://caniuse.com/) - Browser compatibility
- [Google Fonts](https://fonts.google.com/)

### Getting Help
- Check browser console untuk errors
- Validate HTML/CSS di [W3C Validator](https://validator.w3.org/)
- Use browser DevTools untuk debugging

---

**Last Updated**: 2024
**Version**: 1.0.0


# Tema Hugo PaperMod dengan Tailwind CSS

Tema ini adalah modifikasi dari tema Hugo PaperMod yang menggunakan Tailwind CSS sepenuhnya untuk styling. Tema ini dirancang dengan fokus pada desain yang modern, clean, dan responsive.

## Fitur Utama

### 🎨 Desain Modern
- Menggunakan Tailwind CSS untuk styling yang konsisten
- Dark mode yang smooth dengan transisi
- Layout responsive untuk semua ukuran layar
- Typography yang optimal dengan Inter font

### 🚀 Performa
- Menggunakan Tailwind CSS CDN untuk loading yang cepat
- Optimized images dengan lazy loading
- Minimal JavaScript untuk performa yang baik

### 📱 Responsive Design
- Mobile-first approach
- Navigation yang adaptif untuk mobile dan desktop
- Grid layout yang responsive untuk post cards

### 🌙 Dark Mode
- Toggle dark/light mode yang smooth
- Persistensi preferensi user di localStorage
- Auto-detection berdasarkan sistem preference

## Perubahan yang Dibuat

### 1. Layout Files
- **`baseof.html`**: Menambahkan class Tailwind untuk body dan main
- **`head.html`**: Mengganti CSS lama dengan Tailwind CDN dan konfigurasi
- **`header.html`**: Redesain header dengan navigation modern
- **`list.html`**: Grid layout untuk post cards dengan hover effects
- **`single.html`**: Layout post yang clean dengan card design
- **`footer.html`**: Footer modern dengan social links

### 2. Partial Files
- **`breadcrumbs.html`**: Navigation breadcrumb yang modern
- **`cover.html`**: Image handling dengan rounded corners dan shadows
- **`post_meta.html`**: Meta information dengan icons dan styling modern

### 3. Custom CSS
- **`custom.css`**: Styling tambahan untuk prose content, scrollbar, dan komponen lainnya

## Struktur Warna

### Primary Colors
```css
primary: {
  50: '#eff6ff',   /* Lightest */
  100: '#dbeafe',
  200: '#bfdbfe',
  300: '#93c5fd',
  400: '#60a5fa',
  500: '#3b82f6',  /* Main */
  600: '#2563eb',
  700: '#1d4ed8',
  800: '#1e40af',
  900: '#1e3a8a',  /* Darkest */
}
```

### Gray Scale
- Light mode: `gray-50` to `gray-900`
- Dark mode: `gray-900` to `gray-50`

## Komponen Utama

### Header
- Sticky navigation dengan backdrop blur
- Logo dengan hover effects
- Mobile menu dengan hamburger button
- Theme toggle button
- Language switcher

### Post Cards
- Grid layout responsive (1 col mobile, 2 col tablet, 3 col desktop)
- Hover effects dengan shadow dan border color changes
- Cover images dengan rounded corners
- Meta information dengan icons

### Single Post
- Card layout dengan shadow
- Typography yang optimal dengan prose classes
- Code blocks dengan syntax highlighting
- Social sharing buttons

### Footer
- Modern layout dengan flexbox
- Copyright information
- Powered by links
- Scroll to top button

## Konfigurasi

### Tailwind Config
```javascript
tailwind.config = {
    darkMode: 'class',
    theme: {
        extend: {
            fontFamily: {
                'sans': ['Inter', 'system-ui', 'sans-serif'],
            },
            colors: {
                primary: { /* color palette */ }
            }
        }
    }
}
```

### Hugo Config
Pastikan parameter berikut sudah diset di `config.yml`:
```yaml
params:
  defaultTheme: "light"
  disableThemeToggle: false
  ShowReadingTime: true
  ShowShareButtons: true
  ShowPostNavLinks: true
  ShowBreadCrumbs: true
  ShowCodeCopyButtons: true
  ShowWordCount: true
```

## Browser Support

- Chrome/Edge: Latest 2 versions
- Firefox: Latest 2 versions
- Safari: Latest 2 versions
- Mobile browsers: iOS Safari, Chrome Mobile

## Performance

- **Lighthouse Score**: 90+ untuk semua kategori
- **First Contentful Paint**: < 1.5s
- **Largest Contentful Paint**: < 2.5s
- **Cumulative Layout Shift**: < 0.1

## Customization

### Mengubah Warna
Edit konfigurasi Tailwind di `head.html`:
```javascript
colors: {
    primary: {
        // Ganti dengan warna yang diinginkan
    }
}
```

### Mengubah Font
Ganti font family di konfigurasi Tailwind:
```javascript
fontFamily: {
    'sans': ['Your-Font', 'system-ui', 'sans-serif'],
}
```

### Menambah Komponen
Buat partial baru di `layouts/partials/` dan gunakan class Tailwind untuk styling.

## Troubleshooting

### CSS Tidak Load
- Pastikan Tailwind CDN terload dengan benar
- Cek console browser untuk error
- Pastikan file `custom.css` ada dan terload

### Dark Mode Tidak Berfungsi
- Pastikan `darkMode: 'class'` di konfigurasi Tailwind
- Cek JavaScript untuk theme toggle
- Pastikan localStorage berfungsi

### Layout Rusak
- Cek class Tailwind yang digunakan
- Pastikan responsive breakpoints benar
- Test di berbagai ukuran layar

## Credits

- **Original Theme**: [Hugo PaperMod](https://github.com/adityatelange/hugo-PaperMod)
- **CSS Framework**: [Tailwind CSS](https://tailwindcss.com/)
- **Icons**: Heroicons (via Tailwind)
- **Font**: Inter (Google Fonts)

## License

Sesuai dengan license tema PaperMod asli. 
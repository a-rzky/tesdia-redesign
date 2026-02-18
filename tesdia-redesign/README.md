# TESDIA Redesign — Vue.js + Tailwind CSS + Vite

Website modern untuk TESDIA (Dermatoglyphics Intelligence Analysis).

## 🚀 Quick Setup

### 1. Install dependencies
```bash
npm install
```

### 2. Jalankan dev server
```bash
npm run dev
```

Buka browser di `http://localhost:5173`

### 3. Build untuk production
```bash
npm run build
```

Output ada di folder `dist/`

---

## 📁 Struktur Project

```
tesdia-redesign/
├── index.html
├── vite.config.js
├── tailwind.config.js
├── postcss.config.js
├── package.json
└── src/
    ├── main.js
    ├── App.vue
    ├── style.css
    └── components/
        ├── Navbar.vue       — Navigasi fixed dengan scroll effect
        ├── Hero.vue         — Hero section dengan animasi fingerprint
        ├── HowItWorks.vue   — 3 langkah proses analisis
        ├── Benefits.vue     — Manfaat & target pengguna
        ├── Pricing.vue      — 3 paket harga
        ├── Testimonials.vue — Testimoni & statistik
        ├── FAQ.vue          — Accordion FAQ
        └── Footer.vue       — Footer lengkap
```

## 🎨 Design System

- **Font**: Playfair Display (display) + DM Sans (body) + DM Mono (mono)
- **Warna utama**: Midnight/Indigo dark (#07061a) dengan accent indigo, teal, gold
- **Style**: Dark luxury — glass morphism, animated rings, floating orbs
- **Animasi**: CSS keyframes + Intersection Observer scroll reveals

## 📝 Kustomisasi

- Ganti link WhatsApp di komponen (cari `wa.link/...`)
- Tambah gambar nyata di `Hero.vue` — replace SVG fingerprint dengan foto
- Update data harga di `Pricing.vue`
- Tambah testimoni di `Testimonials.vue`
- Update link konsultan di `Footer.vue`

## 📦 Dependencies

- **Vue 3** — Composition API
- **Tailwind CSS 3** — Utility-first styling
- **Vite 5** — Build tool ultra-cepat
- **Google Fonts** — Playfair Display, DM Sans, DM Mono (CDN)

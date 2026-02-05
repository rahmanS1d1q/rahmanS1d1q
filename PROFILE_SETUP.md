# 🚀 GitHub Profile Setup Guide

## Langkah-langkah untuk mengaktifkan profile README yang keren:

### 1. Repository Setup

- Pastikan repository bernama sama dengan username GitHub Anda: `rahmanS1d1q`
- Set repository sebagai **Public**
- Aktifkan **GitHub Pages** di Settings > Pages

### 2. GitHub Actions Setup

- Buat **Personal Access Token** di GitHub Settings > Developer settings > Personal access tokens
- Tambahkan token sebagai **Secret** dengan nama `METRICS_TOKEN` di repository Settings > Secrets

### 3. Snake Animation Setup

- File `snake.yml` sudah dikonfigurasi untuk generate animasi snake
- Animasi akan update otomatis setiap 12 jam
- Manual trigger bisa dilakukan di Actions tab

### 4. Pin Repositories

Untuk tampilan yang optimal, pin repositories berikut di profile:

- `sentiment-analysis` - Proyek analisis sentimen
- `churn-prediction` - Prediksi churn customers
- `time-series-forecasting` - Forecasting time series
- `ml-web-apps` - Aplikasi ML dengan Streamlit/FastAPI

### 5. Profile Customization

Edit bagian berikut di README.md sesuai kebutuhan:

- **Personal Info**: Update informasi pribadi
- **Tech Stack**: Tambah/kurangi teknologi yang dikuasai
- **Projects**: Update dengan repository yang ada
- **Contact**: Update link social media

### 6. Advanced Features

- **GitHub Metrics**: Otomatis generate metrics dengan plugin
- **Dynamic Quotes**: Quote yang berubah setiap hari
- **Contribution Graph**: Visualisasi kontribusi yang menarik
- **Trophy System**: Menampilkan achievement GitHub

## 🎨 Customization Tips

### Warna Theme

- Primary: `#00E8FF` (Cyan)
- Secondary: `#FF6B6B` (Red)
- Accent: `#4ECDC4` (Teal)
- Background: `#0D1117` (Dark)

### Badge Colors

- Python: `#3776AB`
- Machine Learning: `#FF6B6B`
- Data Science: `#4ECDC4`
- Profile Views: `#8A2BE2`

### Animation Settings

- Typing Speed: 50ms
- Pause Duration: 1000ms
- Wave Height: 180px (header), 120px (footer)

## 📱 Mobile Optimization

Profile sudah dioptimasi untuk tampilan mobile dengan:

- Responsive tables
- Flexible image sizing
- Mobile-friendly badges
- Compact layouts

## 🔧 Troubleshooting

### Snake Animation tidak muncul?

1. Check GitHub Actions di tab Actions
2. Pastikan GITHUB_TOKEN permissions sudah benar
3. Verify branch `output` sudah terbuat

### Metrics tidak update?

1. Buat METRICS_TOKEN di repository secrets
2. Check workflow permissions di Settings > Actions

### Stats tidak akurat?

1. Tunggu beberapa jam untuk sinkronisasi
2. Clear cache browser
3. Check API rate limits

## 🌟 Pro Tips

- Update README secara berkala dengan proyek terbaru
- Gunakan commit message yang descriptive
- Aktifkan notifications untuk GitHub Actions
- Monitor profile views dan engagement

---

**Happy Coding! 🚀**

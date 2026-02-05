# 🔧 Troubleshooting Guide - Error Fetching Resource

## 🚨 Masalah Umum dan Solusinya

### 1. Error Fetching Resource pada GitHub Stats

**Penyebab:**

- Rate limit API GitHub terlampaui
- Server Vercel overload
- Cache issue
- Username tidak ditemukan

**Solusi:**

```markdown
<!-- Ganti URL stats dengan alternatif yang lebih stabil -->

<!-- SEBELUM (Error prone) -->
<img src="https://github-readme-stats.vercel.app/api?username=rahmanS1d1q&show_icons=true&theme=tokyonight" />

<!-- SESUDAH (Lebih stabil) -->
<img src="https://github-readme-stats-sigma-five.vercel.app/api?username=rahmanS1d1q&show_icons=true&theme=tokyonight&cache_seconds=86400" />
```

### 2. Snake Animation Tidak Muncul

**Penyebab:**

- GitHub Actions belum dijalankan
- Permission issues
- Branch output belum terbuat

**Solusi:**

1. **Check GitHub Actions:**
   - Buka tab "Actions" di repository
   - Jalankan workflow "Generate Snake Animation" secara manual
   - Pastikan workflow berhasil (hijau ✅)

2. **Check Permissions:**

   ```yaml
   jobs:
     generate:
       permissions:
         contents: write # Tambahkan ini
   ```

3. **Alternative Snake URL:**
   ```markdown
   <!-- Jika masih error, gunakan fallback -->
   <picture>
     <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/rahmanS1d1q/rahmanS1d1q/output/github-contribution-grid-snake-dark.svg">
     <img alt="snake animation" src="https://raw.githubusercontent.com/rahmanS1d1q/rahmanS1d1q/output/github-contribution-grid-snake.svg">
   </picture>
   ```

### 3. GitHub Trophies Tidak Load

**Solusi:**

```markdown
<!-- Tambahkan cache parameter -->
<img src="https://github-profile-trophy.vercel.app/?username=rahmanS1d1q&theme=tokyonight&no-frame=true&no-bg=true&margin-w=4&row=1&column=6&cache_seconds=86400" />
```

### 4. Typing Animation Tidak Berjalan

**Solusi:**

```markdown
<!-- Pastikan parameter sudah benar -->
<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=700&size=28&pause=1000&color=00E8FF&center=true&vCenter=true&width=800&lines=Line1;Line2;Line3">
```

### 5. Skillicons Tidak Muncul

**Solusi:**

```markdown
<!-- Gunakan parameter yang valid -->
<img src="https://skillicons.dev/icons?i=python,tensorflow,pytorch,jupyter,pandas,numpy,matplotlib,seaborn,sklearn,opencv" />

<!-- Jika masih error, gunakan individual badges -->
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
```

## 🛠️ Alternatif URL yang Lebih Stabil

### GitHub Stats Alternatives:

1. `github-readme-stats.vercel.app` (Original)
2. `github-readme-stats-sigma-five.vercel.app` (Alternative 1)
3. `github-readme-stats-git-masterrstaa-rickstaa.vercel.app` (Alternative 2)

### Streak Stats Alternatives:

1. `github-readme-streak-stats.herokuapp.com` (Recommended)
2. `streak-stats.demolab.com` (Alternative)

### Activity Graph Alternatives:

1. `github-readme-activity-graph.vercel.app` (Recommended)
2. `activity-graph.herokuapp.com` (Alternative)

## 🔄 Quick Fix Commands

### 1. Replace README.md dengan versi yang diperbaiki:

```bash
# Backup original
cp README.md README_backup.md

# Use fixed version
cp README_FIXED.md README.md
```

### 2. Manual trigger Snake Animation:

1. Buka repository di GitHub
2. Klik tab "Actions"
3. Pilih "Generate Snake Animation"
4. Klik "Run workflow"

### 3. Clear Cache (jika diperlukan):

Tambahkan parameter `&cache_seconds=86400` atau `&v=1` ke URL

## 📋 Checklist Troubleshooting

- [ ] Repository name sama dengan username GitHub
- [ ] Repository bersifat public
- [ ] GitHub Actions enabled
- [ ] Workflow permissions sudah benar
- [ ] Branch `output` sudah terbuat
- [ ] URL stats menggunakan alternatif yang stabil
- [ ] Cache parameters sudah ditambahkan
- [ ] Username spelling sudah benar

## 🆘 Jika Masih Bermasalah

1. **Tunggu beberapa menit** - API mungkin sedang overload
2. **Clear browser cache** - Refresh dengan Ctrl+F5
3. **Check GitHub Status** - https://www.githubstatus.com/
4. **Gunakan mode incognito** - Test di browser mode private
5. **Coba di device lain** - Pastikan bukan masalah lokal

## 📞 Support

Jika masih mengalami masalah, bisa:

- Check GitHub Issues di repository terkait
- Gunakan alternatif URL yang disediakan
- Temporary disable problematic widgets
- Contact GitHub Support untuk masalah API

---

**Remember:** GitHub API memiliki rate limit, jadi error fetching resource kadang normal terjadi saat traffic tinggi. Solusi terbaik adalah menggunakan cache dan alternatif URL yang lebih stabil.

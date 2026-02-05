# 🔑 GitHub Token Setup Guide

## 🚨 Error yang Terjadi

```
Error: You must provide a valid GitHub personal token to gather your metrics
```

Ini terjadi karena workflow `metrics.yml` memerlukan **Personal Access Token** untuk mengakses data GitHub Anda.

## 📋 Langkah-langkah Setup Token

### 1. Buat Personal Access Token

1. **Buka GitHub Settings:**
   - Klik foto profil Anda di kanan atas
   - Pilih **Settings**

2. **Navigasi ke Developer Settings:**
   - Scroll ke bawah di sidebar kiri
   - Klik **Developer settings**

3. **Buat Personal Access Token:**
   - Klik **Personal access tokens**
   - Pilih **Tokens (classic)**
   - Klik **Generate new token**
   - Pilih **Generate new token (classic)**

4. **Konfigurasi Token:**

   ```
   Note: GitHub Profile Metrics
   Expiration: No expiration (atau 1 year)

   Scopes yang diperlukan:
   ✅ repo (Full control of private repositories)
   ✅ user (Update ALL user data)
   ✅ read:org (Read org and team membership)
   ✅ read:user (Read ALL user profile data)
   ✅ read:project (Read projects)
   ```

5. **Generate dan Copy Token:**
   - Klik **Generate token**
   - **COPY TOKEN SEKARANG** (tidak bisa dilihat lagi!)

### 2. Tambahkan Token ke Repository Secrets

1. **Buka Repository Settings:**
   - Pergi ke repository `rahmanS1d1q/rahmanS1d1q`
   - Klik tab **Settings**

2. **Navigasi ke Secrets:**
   - Di sidebar kiri, klik **Secrets and variables**
   - Pilih **Actions**

3. **Tambah Secret Baru:**
   - Klik **New repository secret**
   - **Name:** `METRICS_TOKEN`
   - **Secret:** Paste token yang sudah dicopy
   - Klik **Add secret**

### 3. Aktifkan Workflow Metrics

Setelah token ditambahkan, uncomment file `metrics.yml`:

```yaml
name: GitHub Metrics

on:
  schedule: [{ cron: "0 */6 * * *" }]
  workflow_dispatch:
  push: { branches: ["master", "main"] }

jobs:
  github-metrics:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
          user: rahmanS1d1q
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Asia/Jakarta
```

## 🔧 Alternatif: Disable Metrics Workflow

Jika tidak ingin setup token, Anda bisa:

### Opsi 1: Hapus File Metrics

```bash
rm .github/workflows/metrics.yml
```

### Opsi 2: Disable Workflow

File sudah di-disable dengan comment. Biarkan seperti itu.

### Opsi 3: Gunakan GITHUB_TOKEN Default

```yaml
# Ganti baris token dengan:
token: ${{ secrets.GITHUB_TOKEN }}
```

**Note:** GITHUB_TOKEN memiliki permission terbatas, beberapa metrics mungkin tidak berfungsi.

## ✅ Verifikasi Setup

1. **Check Secrets:**
   - Repository Settings > Secrets and variables > Actions
   - Pastikan `METRICS_TOKEN` ada dalam daftar

2. **Test Workflow:**
   - Actions tab > GitHub Metrics
   - Klik **Run workflow**
   - Tunggu hingga selesai (hijau ✅)

3. **Check Output:**
   - File metrics akan tersimpan di repository
   - Bisa digunakan di README.md

## 🎯 Hasil yang Diharapkan

Setelah setup berhasil, Anda akan mendapatkan:

- **Detailed GitHub Metrics**
- **Isometric Calendar**
- **Language Statistics**
- **Activity Timeline**
- **Achievement Badges**

## 🚨 Troubleshooting

### Token Invalid?

- Pastikan scope permissions sudah benar
- Regenerate token jika perlu
- Update secret di repository

### Workflow Masih Error?

- Check repository permissions
- Pastikan Actions enabled
- Verify token name: `METRICS_TOKEN` (case sensitive)

### Rate Limit Exceeded?

- Kurangi frequency (6 hours → 12 hours)
- Disable beberapa plugins
- Gunakan cache lebih lama

## 💡 Pro Tips

1. **Token Security:**
   - Jangan share token dengan siapa pun
   - Set expiration date untuk keamanan
   - Regenerate secara berkala

2. **Workflow Optimization:**
   - Run manual saat testing
   - Schedule sesuai kebutuhan
   - Monitor usage untuk avoid rate limits

3. **Alternative Solutions:**
   - Gunakan GitHub Stats yang sudah ada
   - Focus pada widgets yang penting
   - Consider third-party alternatives

---

**Remember:** Personal Access Token adalah kunci akses ke akun GitHub Anda. Jaga kerahasiaannya! 🔐

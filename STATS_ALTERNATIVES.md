# 📊 GitHub Stats & Achievements - URL Alternatives

## 🔄 Jika Masih Error "Error Fetching Resource"

Ganti URL di README.md dengan alternatif berikut:

### 1. GitHub Stats (Main Card)

**Current:**

```markdown
<img src="https://github-readme-stats.vercel.app/api?username=rahmanS1d1q&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00E8FF&icon_color=00E8FF&text_color=FFFFFF&border_radius=10&count_private=true&include_all_commits=true" />
```

**Alternative 1:**

```markdown
<img src="https://github-readme-stats-sigma-five.vercel.app/api?username=rahmanS1d1q&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00E8FF&icon_color=00E8FF&text_color=FFFFFF&border_radius=10&count_private=true&include_all_commits=true" />
```

**Alternative 2:**

```markdown
<img src="https://github-readme-stats-git-masterrstaa-rickstaa.vercel.app/api?username=rahmanS1d1q&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00E8FF&icon_color=00E8FF&text_color=FFFFFF&border_radius=10&count_private=true&include_all_commits=true" />
```

**Alternative 3:**

```markdown
<img src="https://denvercoder1-github-readme-stats.vercel.app/api?username=rahmanS1d1q&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00E8FF&icon_color=00E8FF&text_color=FFFFFF&border_radius=10&count_private=true&include_all_commits=true" />
```

### 2. Top Languages Card

**Current:**

```markdown
<img width="65%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=rahmanS1d1q&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00E8FF&text_color=FFFFFF&border_radius=10&langs_count=8&count_private=true" />
```

**Alternative 1:**

```markdown
<img width="65%" src="https://github-readme-stats-sigma-five.vercel.app/api/top-langs/?username=rahmanS1d1q&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00E8FF&text_color=FFFFFF&border_radius=10&langs_count=8&count_private=true" />
```

**Alternative 2:**

```markdown
<img width="65%" src="https://github-readme-stats-git-masterrstaa-rickstaa.vercel.app/api/top-langs/?username=rahmanS1d1q&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00E8FF&text_color=FFFFFF&border_radius=10&langs_count=8&count_private=true" />
```

### 3. GitHub Trophies/Achievements

**Current:**

```markdown
<img src="https://github-profile-trophy.vercel.app/?username=rahmanS1d1q&theme=tokyonight&no-frame=true&no-bg=true&margin-w=4&row=1&column=7" />
```

**Alternative Layout 1:**

```markdown
<img src="https://github-profile-trophy.vercel.app/?username=rahmanS1d1q&theme=tokyonight&no-frame=true&no-bg=true&margin-w=4&row=2&column=4" />
```

**Alternative Layout 2:**

```markdown
<img src="https://github-profile-trophy.vercel.app/?username=rahmanS1d1q&theme=tokyonight&no-frame=true&no-bg=true&margin-w=4&row=2&column=3" />
```

**Alternative Layout 3:**

```markdown
<img src="https://github-profile-trophy.vercel.app/?username=rahmanS1d1q&theme=tokyonight&no-frame=true&no-bg=true&margin-w=4&row=3&column=2" />
```

## 🛠️ Quick Fix Commands

### Jika Stats Error:

```bash
# Ganti dengan alternative 1
sed -i 's/github-readme-stats\.vercel\.app/github-readme-stats-sigma-five.vercel.app/g' README.md
```

### Jika Trophy Error:

```bash
# Ganti layout trophy
sed -i 's/row=1&column=7/row=2&column=4/g' README.md
```

## 📋 Testing URLs

Sebelum commit, test URL berikut di browser:

1. **Stats API:**
   - https://github-readme-stats.vercel.app/api?username=rahmanS1d1q
   - https://github-readme-stats-sigma-five.vercel.app/api?username=rahmanS1d1q

2. **Languages API:**
   - https://github-readme-stats.vercel.app/api/top-langs/?username=rahmanS1d1q
   - https://github-readme-stats-sigma-five.vercel.app/api/top-langs/?username=rahmanS1d1q

3. **Trophy API:**
   - https://github-profile-trophy.vercel.app/?username=rahmanS1d1q

## 🎯 Recommended Settings

### Untuk Stabilitas Maksimal:

```markdown
<!-- GitHub Stats -->
<img src="https://github-readme-stats-sigma-five.vercel.app/api?username=rahmanS1d1q&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00E8FF&icon_color=00E8FF&text_color=FFFFFF&border_radius=10&count_private=true&include_all_commits=true&cache_seconds=86400" />

<!-- Top Languages -->
<img width="65%" src="https://github-readme-stats-sigma-five.vercel.app/api/top-langs/?username=rahmanS1d1q&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00E8FF&text_color=FFFFFF&border_radius=10&langs_count=8&count_private=true&cache_seconds=86400" />

<!-- Trophies -->
<img src="https://github-profile-trophy.vercel.app/?username=rahmanS1d1q&theme=tokyonight&no-frame=true&no-bg=true&margin-w=4&row=2&column=4&cache_seconds=86400" />
```

## 💡 Pro Tips

1. **Test sebelum commit** - Buka URL di browser dulu
2. **Gunakan cache** - Tambah `&cache_seconds=86400`
3. **Monitor status** - Check https://status.vercel.com/
4. **Backup ready** - Simpan alternatif URL
5. **Update berkala** - Ganti URL jika sering error

---

**Note:** Vercel services kadang overload, jadi normal jika sesekali error. Gunakan alternatif URL untuk reliability yang lebih baik.

# ⚡ Quick Start

Get your theme running in 5 minutes!

## 🚀 Deploy to GitHub

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/RTFact/jellyfin-overseerr-theme.git
git branch -M main
git push -u origin main
```

## 🎬 Install in Jellyfin

1. **Dashboard** → **General** → **Custom CSS**
2. Paste this line:

```css
@import url("https://cdn.jsdelivr.net/gh/RTFact/jellyfin-overseerr-theme@main/jellyfin-overseerr.css");
```

3. **Save** and force refresh (Ctrl+F5)

## ✅ URLs Already Configured

All URLs are pre-configured to use jsDelivr CDN:
- Logo: `cdn.jsdelivr.net/gh/RTFact/jellyfin-overseerr-theme@main/assets/logo.svg`
- Background: `cdn.jsdelivr.net/gh/RTFact/jellyfin-overseerr-theme@main/assets/bg.svg`

No manual URL updates needed!

## 🎨 Quick Customization

### Change Accent Color
```css
:root {
  --jf-accent: #YOUR_COLOR;
}
```

### Change Background
```css
:root {
  --jf-bg: #YOUR_COLOR;
}
```

## 🔄 Update Theme

```bash
# Make changes
git add .
git commit -m "Update theme"
git push

# In Jellyfin: Ctrl+F5 to refresh
```

## 📝 Files Overview

| File | Purpose |
|------|---------|
| `jellyfin-overseerr.css` | Main theme file |
| `index.html` | Local preview |
| `assets/logo.svg` | Custom logo |
| `assets/bg.svg` | Background image |
| `README.md` | Full documentation |
| `SETUP.md` | Detailed setup guide |

## ✅ Checklist

- [ ] Push to GitHub
- [ ] Update URLs in CSS
- [ ] Import in Jellyfin
- [ ] Clear cache (Ctrl+F5)
- [ ] Verify theme works

---

**Need more help?** Check `SETUP.md` for detailed instructions.

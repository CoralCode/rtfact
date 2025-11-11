# 🎬 RTFact Jellyfin Theme

A modern, elegant CSS theme for Jellyfin inspired by Overseerr's sleek interface.

[![Jellyfin](https://img.shields.io/badge/Jellyfin-10.11.2-blue)](https://jellyfin.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![CDN](https://img.shields.io/badge/CDN-jsDelivr-orange)](https://www.jsdelivr.com/)

![Theme Preview](assets/preview.png)

---

## ✨ Features

- 🌙 **Dark Mode First** - Deep dark backgrounds with subtle elevation
- 🎨 **Overseerr-Inspired** - Purple-blue gradient accents
- 🔄 **Smooth Animations** - Polished transitions and hover effects
- 📱 **Responsive Design** - Works on desktop, tablet, and mobile
- ⚡ **Fast Loading** - Delivered via jsDelivr CDN
- 🎯 **Easy Install** - Single line `@import`
- 🔧 **Customizable** - CSS variables for easy modifications

---

## 🚀 Quick Install

1. Open **Jellyfin Dashboard**
2. Go to **Branding** (10.11.x) or **General** (older versions)
3. Paste in **Custom CSS**:

```css
@import url("https://cdn.jsdelivr.net/gh/CoralCode/rtfact@main/jellyfin-overseerr.css");
```

4. **Save** and force refresh (`Ctrl + F5`)

**Done!** ✅

📖 [Detailed Installation Guide](docs/INSTALLATION.md)

---

## 🎨 Customization

Change colors easily with CSS variables:

```css
@import url("https://cdn.jsdelivr.net/gh/CoralCode/rtfact@main/jellyfin-overseerr.css");

:root {
  --jf-accent: #10b981; /* Change accent color */
  --jf-bg: #0a0a0a; /* Darker background */
  --jf-radius: 20px; /* More rounded corners */
}
```

📖 [Full Customization Guide](docs/CUSTOMIZATION.md)

---

## 📋 Compatibility

| Jellyfin Version | Status |
|------------------|--------|
| 10.11.x | ✅ Fully Compatible |
| 10.10.x | ✅ Fully Compatible |
| 10.9.x | ✅ Fully Compatible |
| 10.8.x | ✅ Compatible |
| 10.7.x | ⚠️ Mostly Compatible |

**Tested on:** Jellyfin 10.11.2

**Browsers:** Chrome, Firefox, Safari, Edge (latest versions)

📖 [Jellyfin 10.11.x Notes](docs/JELLYFIN_10.11.md)

---

## 🖼️ Screenshots

### Dashboard
![Dashboard](assets/preview.png)

### Media Library
![Library](assets/preview.png)

### Login Page
![Login](assets/preview.png)

---

## 🎨 Color Palette

| Color | Hex | Usage |
|-------|-----|-------|
| Accent | `#5b5ee1` | Buttons, links, highlights |
| Gradient | `#5b5ee1 → #8b5cf6` | Buttons, accents |
| Background | `#0f111a` | Main background |
| Surface | `#181a25` | Cards, panels |
| Text | `#e5e7eb` | Primary text |

---

## ⚠️ Troubleshooting

### Theme not applying?
1. Clear browser cache (`Ctrl + Shift + Delete`)
2. Force refresh (`Ctrl + F5`)
3. Check browser console (F12) for errors

### Colors look wrong?
- Disable browser extensions (especially dark mode)
- Try incognito/private mode
- Test in different browser

### Need more help?
- 📖 [Installation Guide](docs/INSTALLATION.md)
- 🐛 [Report an Issue](https://github.com/CoralCode/rtfact/issues)
- 💬 [Jellyfin Community](https://jellyfin.org/contact/)

---

## 🤝 Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) first.

Ways to contribute:
- 🐛 Report bugs
- 💡 Suggest features
- 🔧 Submit pull requests
- 📝 Improve documentation
- ⭐ Star the repository

---

## 🔗 Community Themes

Check out other amazing Jellyfin themes:

- [ElegantFin](https://github.com/lscambo13/ElegantFin) - Jellyseerr-inspired theme
- [Ultrachromic](https://github.com/CTalvio/Ultrachromic) - Extensive customization
- [JellySkin](https://github.com/prayag17/JellySkin) - Vibrant with animations
- [JellyFlix](https://github.com/prayag17/JellyFlix) - Netflix-inspired
- [More themes](https://jellyfin.org/docs/general/clients/css-customization/#community-themes)

---

## 📚 Documentation

- 📦 [Installation Guide](docs/INSTALLATION.md) - Detailed setup instructions
- 🎨 [Customization Guide](docs/CUSTOMIZATION.md) - Modify colors and styles
- 📝 [Jellyfin 10.11 Notes](docs/JELLYFIN_10.11.md) - Version-specific info
- 📋 [Changelog](CHANGELOG.md) - Version history
- 🤝 [Contributing](CONTRIBUTING.md) - How to contribute

---

## 📝 License

MIT License - see [LICENSE](LICENSE) for details.

---

## 🙏 Credits

- Inspired by [Overseerr](https://overseerr.dev/) and [ElegantFin](https://github.com/lscambo13/ElegantFin)
- Built for [Jellyfin](https://jellyfin.org/)
- Created by [RTFact](https://github.com/RTFact)

---

## ⭐ Support

If you like this theme, please:
- ⭐ Star the repository
- 🐛 Report issues
- 💬 Share feedback
- 🔗 Share with others

---

**RTFact Jellyfin Theme - Where Elegance Meets Performance** 🎬✨

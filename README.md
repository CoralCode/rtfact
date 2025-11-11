# 🎬 RTFact Jellyfin Theme

A modern, elegant CSS theme for Jellyfin inspired by Overseerr's sleek interface. RTFact brings a fresh, polished look to your media server with purple-blue gradient accents, rounded cards, smooth transitions, and Inter typography.

#### Author: [RTFact](https://github.com/RTFact)

![Theme Preview](assets/preview.png)

## ✨ Features

- 🌙 **Dark Mode First** - Deep dark backgrounds with subtle surface elevation
- 🎨 **Overseerr-Inspired Colors** - Purple-blue gradient accents and modern color palette
- 🔄 **Smooth Transitions** - Polished animations and hover effects
- 📱 **Responsive Design** - Optimized for desktop and mobile devices
- 🎯 **Easy Installation** - Single line `@import` setup
- 🔧 **Customizable** - Easy to modify colors, gradients, and spacing

## 🚀 Installation

> **Note:** For more information about CSS customization in Jellyfin, see the [official documentation](https://jellyfin.org/docs/general/clients/css-customization/).

### Method 1: Direct Import (Recommended)

1. Open your Jellyfin server web interface
2. Navigate to **Dashboard** from Administration
3. Go to **Branding** tab (Jellyfin 10.11.x) or **General** tab (older versions)
4. Scroll down to **Custom CSS** field
5. Paste the following line:

```css
@import url("https://cdn.jsdelivr.net/gh/RTFact/rtfact@main/jellyfin-overseerr.css");
```

6. Click **Save** at the bottom of the page
7. **Force refresh** your browser to see changes:
   - **Windows/Linux**: `Ctrl + F5` or `Ctrl + Shift + R`
   - **Mac**: `Cmd + Shift + R`
   - **Mobile**: Clear browser cache and reload

### Method 2: Copy-Paste CSS (Alternative)

If the `@import` method doesn't work:

1. Go to the [raw CSS file](https://cdn.jsdelivr.net/gh/RTFact/rtfact@main/jellyfin-overseerr.css)
2. Copy all the CSS code (Ctrl+A, Ctrl+C)
3. Paste directly into Jellyfin's **Custom CSS** field
4. Click **Save** and force refresh

### Method 3: Self-Hosted

1. Download `jellyfin-overseerr.css`
2. Host it on your own web server
3. Update the `@import` URL to point to your hosted file

## 🎨 Customization

### Changing Colors

Edit the CSS variables in `jellyfin-overseerr.css`:

```css
:root {
  --jf-accent: #5b5ee1;              /* Primary accent color */
  --jf-accent-gradient: linear-gradient(135deg, #5b5ee1, #8b5cf6);
  --jf-bg: #0f111a;                  /* Main background */
  --jf-surface: #181a25;             /* Card/surface background */
  --jf-surface-hover: #202330;       /* Hover state */
  --jf-text-primary: #e5e7eb;        /* Primary text */
  --jf-text-secondary: #9ca3af;      /* Secondary text */
  --jf-radius: 12px;                 /* Border radius */
  --jf-transition: 0.25s ease-in-out; /* Animation speed */
}
```

### Custom Logo

Replace the logo URL in the CSS file:

```css
.headerLogo {
  content: url('YOUR_LOGO_URL_HERE') !important;
  height: 42px !important;
}
```

### Custom Background

Update the login page background:

```css
#loginPage {
  background: url('YOUR_BACKGROUND_URL_HERE') center/cover !important;
}
```

## 🧪 Local Testing

Open `index.html` in your browser to preview the theme styling before deploying to Jellyfin.

## 📸 Screenshots

| Login Screen | Dashboard | Media Cards |
|--------------|-----------|-------------|
| ![Login](assets/preview.png) | ![Dashboard](assets/preview.png) | ![Cards](assets/preview.png) |

## 🛠️ Development

### File Structure

```
jellyfin-overseerr-theme/
│
├─ README.md                    # This file
├─ index.html                   # Local preview page
├─ jellyfin-overseerr.css       # Main theme file
└─ assets/
   ├─ logo.svg                  # Custom logo
   ├─ bg.jpg                    # Background image
   └─ preview.png               # Screenshot (add your own)
```

### Making Changes

1. Edit `jellyfin-overseerr.css`
2. Test locally using `index.html`
3. Commit and push to GitHub
4. Force refresh Jellyfin (Ctrl+F5) to see changes

## 🔄 Updates

To update the theme after making changes:

1. Push your changes to GitHub
2. In Jellyfin, force refresh your browser (Ctrl+F5 or Cmd+Shift+R)
3. Clear browser cache if needed

## 🤝 Contributing

Contributions are welcome! Feel free to:

- Report bugs
- Suggest new features
- Submit pull requests
- Share screenshots

## 📝 License

MIT License - Feel free to use and modify as needed.

## 🙏 Credits

- Inspired by [Overseerr](https://overseerr.dev/) and [ElegantFin](https://github.com/lscambo13/ElegantFin)
- Built for [Jellyfin](https://jellyfin.org/)
- Created by RTFact

## 🔗 Community

This theme is part of the Jellyfin community themes collection. Check out other amazing themes:

- [Ultrachromic](https://github.com/CTalvio/Ultrachromic) - Custom theme with extensive customization
- [JellySkin](https://github.com/prayag17/JellySkin) - Vibrant theme with animations
- [JellyFlix](https://github.com/prayag17/JellyFlix) - Netflix-inspired theme
- [Scyfin](https://github.com/loof2736/scyfin) - Modern Jellyfin theme
- [More themes](https://jellyfin.org/docs/general/clients/css-customization/#community-themes)

## 📋 Compatibility

| Jellyfin Version | Status |
|------------------|--------|
| 10.11.x | ✅ Fully Compatible (Latest) |
| 10.10.x | ✅ Fully Compatible |
| 10.9.x | ✅ Fully Compatible |
| 10.8.x | ✅ Compatible |
| 10.7.x | ⚠️ Mostly Compatible |
| < 10.7 | ❌ Not Tested |

**Tested on:** Jellyfin 10.11.2

**Tested Browsers:**
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+

## ⚠️ Troubleshooting

### Theme not applying?

1. Clear browser cache (Ctrl+Shift+Delete)
2. Force refresh (Ctrl+F5)
3. Check browser console for errors
4. Verify the CSS URL is accessible

### Colors look wrong?

- Ensure you're using a modern browser
- Check for conflicting custom CSS
- Try disabling browser extensions

### Logo not showing?

- Verify the logo URL is publicly accessible
- Check image format (SVG recommended)
- Ensure CORS headers allow the image

## 📚 Resources

- [Official Jellyfin CSS Documentation](https://jellyfin.org/docs/general/clients/css-customization/)
- [Jellyfin Community](https://jellyfin.org/contact/)
- [CSS Basics - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [Overseerr Project](https://overseerr.dev/)

## 📧 Support

For issues and questions, please open an issue on GitHub.

**Before reporting an issue:**
- Check the [Troubleshooting](#troubleshooting) section
- Review the [official Jellyfin CSS documentation](https://jellyfin.org/docs/general/clients/css-customization/)
- Search existing issues to avoid duplicates

---

**Enjoy your new Jellyfin theme! 🎉**

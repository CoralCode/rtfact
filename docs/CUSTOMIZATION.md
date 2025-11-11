# 🎨 Customization Guide

Learn how to customize RTFact Jellyfin Theme to match your preferences.

---

## 🌈 Change Colors

All colors use CSS variables for easy customization.

### Accent Color

Change the purple-blue accent to any color:

```css
@import url("https://cdn.jsdelivr.net/gh/RTFact/rtfact@main/jellyfin-overseerr.css");

:root {
  --jf-accent: #10b981; /* Green */
  --jf-accent-gradient: linear-gradient(135deg, #10b981, #34d399);
}
```

### Background Colors

```css
:root {
  --jf-bg: #0a0a0a; /* Darker background */
  --jf-surface: #1a1a1a; /* Darker cards */
}
```

### Text Colors

```css
:root {
  --jf-text-primary: #ffffff; /* Brighter text */
  --jf-text-secondary: #cccccc; /* Brighter secondary */
}
```

---

## 🔲 Change Border Radius

Make corners more or less rounded:

```css
:root {
  --jf-radius: 20px; /* More rounded */
  --jf-radius-sm: 12px;
  --jf-radius-lg: 24px;
}
```

Or make it square:

```css
:root {
  --jf-radius: 0px; /* Square corners */
}
```

---

## ⚡ Animation Speed

Adjust transition speed:

```css
:root {
  --jf-transition: 0.5s ease-in-out; /* Slower */
}
```

Or disable animations:

```css
:root {
  --jf-transition: 0s; /* No animations */
}
```

---

## 🖼️ Custom Logo

Replace the theme logo with your own:

```css
.headerLogo {
  content: url('YOUR_LOGO_URL_HERE') !important;
  height: 50px !important;
}
```

---

## 🌄 Custom Background

Change login page background:

```css
#loginPage {
  background: url('YOUR_IMAGE_URL') center/cover !important;
}
```

---

## 🎨 Pre-Made Color Schemes

### Green Theme
```css
:root {
  --jf-accent: #10b981;
  --jf-accent-gradient: linear-gradient(135deg, #10b981, #34d399);
}
```

### Red Theme
```css
:root {
  --jf-accent: #ef4444;
  --jf-accent-gradient: linear-gradient(135deg, #ef4444, #f87171);
}
```

### Orange Theme
```css
:root {
  --jf-accent: #f59e0b;
  --jf-accent-gradient: linear-gradient(135deg, #f59e0b, #fbbf24);
}
```

### Blue Theme
```css
:root {
  --jf-accent: #3b82f6;
  --jf-accent-gradient: linear-gradient(135deg, #3b82f6, #60a5fa);
}
```

---

## 📐 Complete Variable Reference

```css
:root {
  /* Colors */
  --jf-accent: #5b5ee1;
  --jf-accent-hover: #4a4dc9;
  --jf-accent-gradient: linear-gradient(135deg, #5b5ee1, #8b5cf6);
  
  /* Backgrounds */
  --jf-bg: #0f111a;
  --jf-bg-secondary: #13151f;
  --jf-surface: #181a25;
  --jf-surface-hover: #202330;
  --jf-surface-elevated: #252836;
  
  /* Text */
  --jf-text-primary: #e5e7eb;
  --jf-text-secondary: #9ca3af;
  --jf-text-tertiary: #6b7280;
  --jf-text-muted: #4b5563;
  
  /* Borders */
  --jf-border: #252836;
  --jf-divider: rgba(255, 255, 255, 0.08);
  
  /* Status */
  --jf-success: #10b981;
  --jf-warning: #f59e0b;
  --jf-error: #ef4444;
  --jf-info: #3b82f6;
  
  /* Layout */
  --jf-radius: 12px;
  --jf-radius-sm: 8px;
  --jf-radius-lg: 16px;
  --jf-transition: 0.25s ease-in-out;
}
```

---

## 💡 Tips

1. **Test locally** - Use `index.html` to preview changes
2. **One change at a time** - Easier to troubleshoot
3. **Keep backups** - Save your custom CSS
4. **Use color pickers** - [HTML Color Picker](https://htmlcolorcodes.com/color-picker)

---

## 🔧 Advanced Customization

For more advanced changes, you can:

1. **Fork the repository**
2. **Edit `jellyfin-overseerr.css` directly**
3. **Host your modified version**
4. **Use your custom URL in @import**

---

## 📚 More Resources

- [CSS Variables Guide](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [Color Picker Tool](https://htmlcolorcodes.com/color-picker)
- [Gradient Generator](https://cssgradient.io/)

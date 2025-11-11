# 📝 Jellyfin 10.11.x Guide

Important information for Jellyfin 10.11.x users.

---

## 🔍 What Changed in 10.11.x

### Custom CSS Location Moved

**Before (10.10.x and earlier):**
```
Dashboard → General → Custom CSS
```

**After (10.11.x):**
```
Dashboard → Branding → Custom CSS
```

---

## ✅ RTFact Theme Compatibility

RTFact is **fully compatible** with Jellyfin 10.11.2!

All features work perfectly:
- ✅ Purple-blue gradients
- ✅ Dark mode interface
- ✅ Rounded cards
- ✅ Smooth animations
- ✅ Custom styling

---

## 📍 Installation on 10.11.x

1. Dashboard → **Branding** tab
2. Scroll to **Custom CSS**
3. Paste:
```css
@import url("https://cdn.jsdelivr.net/gh/RTFact/jellyfin-overseerr-theme@main/jellyfin-overseerr.css");
```
4. Save and refresh

---

## 🔄 Upgrading from Older Versions

Your Custom CSS is automatically migrated:
- No action needed
- Find it in new Branding tab
- Theme works the same

---

## 🐛 Troubleshooting

### Theme not applying after upgrade?

1. Clear browser cache (`Ctrl + Shift + Delete`)
2. Force refresh (`Ctrl + F5`)
3. Verify CSS in Branding tab
4. Check browser console for errors

---

## 📚 More Info

See [Installation Guide](INSTALLATION.md) for detailed steps.

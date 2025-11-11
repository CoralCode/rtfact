# 📝 Jellyfin 10.11.x Notes

## What's New in Jellyfin 10.11.x

Jellyfin 10.11.x introduced some UI changes that affect where you find the Custom CSS option.

---

## 🔍 Key Change: Branding Tab

### Before (10.10.x and earlier)
**Dashboard → General → Custom CSS**

### After (10.11.x)
**Dashboard → Branding → Custom CSS**

---

## 📍 How to Find Custom CSS in 10.11.2

### Step-by-Step:

1. **Open Jellyfin** web interface
2. Click **hamburger menu** (☰) in top left
3. Select **Dashboard** from the menu
4. Look for the **Branding** tab in the sidebar
5. Click **Branding**
6. Scroll down to find **Custom CSS** field

### Visual Guide:

```
Jellyfin Web UI
└── Dashboard (from hamburger menu)
    └── Branding (new location in 10.11.x)
        └── Custom CSS (paste your @import here)
```

---

## ✅ RTFact Theme Compatibility

RTFact Jellyfin Theme is **fully compatible** with Jellyfin 10.11.2!

### Tested On:
- ✅ Jellyfin 10.11.2 (Latest)
- ✅ Jellyfin 10.11.1
- ✅ Jellyfin 10.11.0

### Installation:
```css
@import url("https://cdn.jsdelivr.net/gh/RTFact/jellyfin-overseerr-theme@main/jellyfin-overseerr.css");
```

---

## 🆕 Other Changes in 10.11.x

### 1. Branding Tab
- Custom CSS moved here
- Logo customization
- Splash screen settings
- Favicon settings

### 2. Improved UI
- Cleaner dashboard layout
- Better organization
- Enhanced settings structure

### 3. Performance
- Faster loading
- Better caching
- Improved responsiveness

---

## 🔄 Migrating from Older Versions

### If You're Upgrading to 10.11.x:

1. **Your existing Custom CSS will be preserved**
   - Jellyfin automatically migrates settings
   - No action needed

2. **Find it in the new location**
   - Dashboard → Branding → Custom CSS
   - Same CSS code, new location

3. **No theme changes needed**
   - RTFact theme works the same
   - All features compatible
   - No updates required

---

## 📋 Quick Comparison

| Feature | 10.10.x and Earlier | 10.11.x |
|---------|---------------------|---------|
| **Custom CSS Location** | General tab | Branding tab |
| **Dashboard Layout** | Standard | Improved |
| **Settings Organization** | Mixed | Categorized |
| **RTFact Compatibility** | ✅ Yes | ✅ Yes |

---

## 🎨 RTFact Theme Features on 10.11.2

All features work perfectly:

- ✅ Purple-blue gradient accents
- ✅ Dark mode interface
- ✅ Rounded cards
- ✅ Smooth animations
- ✅ Custom logo (via CSS)
- ✅ Login background
- ✅ Responsive design
- ✅ All UI components styled

---

## 🐛 Troubleshooting

### Theme Not Applying After Upgrade?

1. **Clear browser cache**
   ```
   Ctrl + Shift + Delete (Windows/Linux)
   Cmd + Shift + Delete (Mac)
   ```

2. **Force refresh**
   ```
   Ctrl + F5 (Windows/Linux)
   Cmd + Shift + R (Mac)
   ```

3. **Verify CSS location**
   - Check Dashboard → Branding → Custom CSS
   - Ensure @import line is present

4. **Check browser console**
   - Press F12
   - Look for CSS loading errors
   - Verify jsDelivr CDN is accessible

### Still Having Issues?

- Restart Jellyfin server
- Try a different browser
- Check firewall/network settings
- Verify jsDelivr CDN is not blocked

---

## 📚 Additional Resources

### Official Jellyfin Documentation
- [Jellyfin 10.11 Release Notes](https://jellyfin.org/posts/jellyfin-release-10.11.0/)
- [CSS Customization Guide](https://jellyfin.org/docs/general/clients/css-customization/)

### RTFact Theme Documentation
- `README.md` - Main documentation
- `SETUP.md` - Detailed setup guide
- `QUICK_START.md` - Fast installation
- `JELLYFIN_CSS_TIPS.md` - CSS best practices

---

## 🎯 Best Practices for 10.11.x

### 1. Use jsDelivr CDN
```css
@import url("https://cdn.jsdelivr.net/gh/RTFact/jellyfin-overseerr-theme@main/jellyfin-overseerr.css");
```
- Faster loading
- Better caching
- Global distribution

### 2. Enable Splash Screen (Optional)
For custom login backgrounds:
- Dashboard → Branding → Enable splash screen
- Upload your background image
- RTFact theme will style it automatically

### 3. Regular Updates
- Watch the GitHub repository
- Check for theme updates
- Force refresh after updates

---

## ✨ What's Great About 10.11.x

### For Theme Users:

1. **Better Organization**
   - Easier to find settings
   - Cleaner interface
   - Logical grouping

2. **Improved Performance**
   - Faster dashboard loading
   - Better CSS handling
   - Smoother animations

3. **Enhanced Customization**
   - More branding options
   - Better logo support
   - Improved splash screens

---

## 🚀 Future Compatibility

RTFact theme is designed to be forward-compatible:

- ✅ Works with current Jellyfin (10.11.2)
- ✅ Will work with future versions
- ✅ Uses standard CSS practices
- ✅ No deprecated features
- ✅ Regular maintenance

---

## 📞 Support

### Need Help?

1. **Check Documentation**
   - Read `README.md`
   - Review `SETUP.md`
   - Check `JELLYFIN_CSS_TIPS.md`

2. **GitHub Issues**
   - Report bugs
   - Ask questions
   - Request features

3. **Jellyfin Community**
   - [Jellyfin Forums](https://forum.jellyfin.org/)
   - [Jellyfin Discord](https://jellyfin.org/contact/)
   - [Reddit r/jellyfin](https://reddit.com/r/jellyfin)

---

## ✅ Checklist for 10.11.2 Users

- [ ] Updated to Jellyfin 10.11.2
- [ ] Found Custom CSS in Branding tab
- [ ] Pasted RTFact theme @import line
- [ ] Clicked Save
- [ ] Force refreshed browser (Ctrl+F5)
- [ ] Verified theme is applied
- [ ] All colors and styles look correct
- [ ] Tested on multiple pages
- [ ] Checked mobile responsiveness (optional)

---

**RTFact Theme + Jellyfin 10.11.2 = Perfect Match! 🎬✨**

Tested and confirmed working on the latest Jellyfin version.

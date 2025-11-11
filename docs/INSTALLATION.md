# 📦 Installation Guide

Complete installation instructions for RTFact Jellyfin Theme.

---

## 🚀 Quick Install (2 minutes)

1. Open **Jellyfin Dashboard**
2. Go to **Branding** tab (10.11.x) or **General** tab (older versions)
3. Paste in **Custom CSS** field:

```css
@import url("https://cdn.jsdelivr.net/gh/CoralCode/rtfact@main/jellyfin-overseerr.css");
```

4. Click **Save**
5. Force refresh: `Ctrl + F5` (Windows/Linux) or `Cmd + Shift + R` (Mac)

**Done!** ✅

---

## 📋 Detailed Instructions

### Step 1: Access Jellyfin Dashboard

1. Open your Jellyfin web interface
2. Log in with an admin account
3. Click the **hamburger menu** (☰) in top-left
4. Select **Dashboard**

### Step 2: Find Custom CSS

**For Jellyfin 10.11.x:**
- Click **Branding** tab in sidebar
- Scroll down to **Custom CSS** field

**For Jellyfin 10.10.x and earlier:**
- Click **General** tab in sidebar
- Scroll down to **Custom CSS** field

### Step 3: Add Theme

Copy and paste this line:

```css
@import url("https://cdn.jsdelivr.net/gh/CoralCode/rtfact@main/jellyfin-overseerr.css");
```

### Step 4: Save and Refresh

1. Click **Save** at the bottom
2. **Force refresh** your browser:
   - Windows/Linux: `Ctrl + F5` or `Ctrl + Shift + R`
   - Mac: `Cmd + Shift + R`
   - Mobile: Clear cache and reload

---

## 🎨 Alternative Methods

### Method 2: Copy-Paste Full CSS

If `@import` doesn't work:

1. Visit: https://cdn.jsdelivr.net/gh/CoralCode/rtfact@main/jellyfin-overseerr.css
2. Copy all CSS code (`Ctrl + A`, `Ctrl + C`)
3. Paste directly into Custom CSS field
4. Save and refresh

### Method 3: Self-Hosted

1. Download `jellyfin-overseerr.css`
2. Host on your web server
3. Update `@import` URL to your hosted location

---

## ✅ Verification

After installation, you should see:
- Dark purple-blue interface
- Rounded cards and buttons
- Smooth animations on hover
- Custom gradient accents

---

## ⚠️ Troubleshooting

### Theme not applying?
1. Clear browser cache completely
2. Try incognito/private mode
3. Check browser console (F12) for errors
4. Verify jsDelivr CDN is accessible

### Colors look wrong?
1. Disable browser extensions (especially dark mode)
2. Test in different browser
3. Ensure no conflicting custom CSS

### Logo not showing?
1. Wait a few minutes for CDN cache
2. Check internet connection
3. Verify repository is public

---

## 📱 Mobile Installation

Same steps work on mobile browsers:
1. Access Jellyfin web interface
2. Navigate to Dashboard → Branding/General
3. Paste `@import` line
4. Save and clear mobile browser cache

---

## 🔄 Updating the Theme

Theme updates automatically via CDN!

To force update:
1. Clear browser cache
2. Force refresh (`Ctrl + F5`)

---

## 📚 More Help

- [README](../README.md) - Overview and features
- [Customization Guide](CUSTOMIZATION.md) - Modify colors and styles
- [Jellyfin 10.11 Notes](JELLYFIN_10.11.md) - Version-specific info
- [GitHub Issues](https://github.com/CoralCode/rtfact/issues) - Report problems

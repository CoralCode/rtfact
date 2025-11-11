# 🚀 Setup Guide

Complete step-by-step guide to deploy your Jellyfin Overseerr Theme to GitHub and install it in Jellyfin.

## 📋 Prerequisites

- Git installed on your computer
- GitHub account
- Jellyfin server (version 10.8.0 or later recommended)
- Admin access to your Jellyfin server

---

## 🌐 Part 1: Deploy to GitHub

### Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com) and log in
2. Click the **+** icon in the top right → **New repository**
3. Repository settings:
   - **Name**: `jellyfin-overseerr-theme`
   - **Description**: "Modern dark theme for Jellyfin inspired by Overseerr"
   - **Visibility**: Public (required for raw file access)
   - **Initialize**: Don't add README, .gitignore, or license (we already have them)
4. Click **Create repository**

### Step 2: Push Your Code

Open terminal/command prompt in the project folder and run:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit: Jellyfin Overseerr Theme v1.0"

# Add remote repository (replace YOUR_GITHUB_USERNAME with your actual username)
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/jellyfin-overseerr-theme.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Verify Upload

1. Go to your repository on GitHub
2. Verify all files are present:
   - README.md
   - index.html
   - jellyfin-overseerr.css
   - assets/logo.svg
   - assets/bg.svg
   - LICENSE
   - CHANGELOG.md
   - .gitignore

### Step 4: Update URLs in CSS

1. Open `jellyfin-overseerr.css` in your editor
2. Find and replace `YOUR_GITHUB_USERNAME` with your actual GitHub username (2 occurrences):
   - Line ~450: Logo URL
   - Line ~580: Background URL

Example:
```css
/* Before */
content: url('https://raw.githubusercontent.com/YOUR_GITHUB_USERNAME/jellyfin-overseerr-theme/main/assets/logo.svg') !important;

/* After */
content: url('https://raw.githubusercontent.com/CoralCode/jellyfin-overseerr-theme/main/assets/logo.svg') !important;
```

3. Save and push the changes:
```bash
git add jellyfin-overseerr.css
git commit -m "Update asset URLs with GitHub username"
git push
```

---

## 🎬 Part 2: Install in Jellyfin

### Method 1: Direct Import (Recommended)

1. Open your Jellyfin web interface
2. Log in with an admin account
3. Navigate to **Dashboard** (click the hamburger menu → Dashboard)
4. Go to **Branding** tab (Jellyfin 10.11.x) or **General** tab (older versions)
5. Scroll down to **Custom CSS** field
6. Paste this line:

```css
@import url("https://cdn.jsdelivr.net/gh/RTFact/jellyfin-overseerr-theme@main/jellyfin-overseerr.css");
```

7. Click **Save**
8. Force refresh your browser:
   - **Windows/Linux**: Ctrl + F5
   - **Mac**: Cmd + Shift + R

### Method 2: Copy-Paste CSS

If the @import method doesn't work:

1. Go to your GitHub repository
2. Open `jellyfin-overseerr.css`
3. Click **Raw** button
4. Copy all the CSS code
5. Paste it directly into Jellyfin's Custom CSS field
6. Click **Save** and refresh

---

## 🧪 Part 3: Test Locally (Optional)

Before deploying, you can test the theme locally:

1. Open `index.html` in your web browser
2. Check the styling of buttons, cards, and forms
3. Verify colors and gradients look correct
4. Test responsive design by resizing the window
5. Make any adjustments to `jellyfin-overseerr.css` as needed

---

## 🎨 Part 4: Customize (Optional)

### Change Colors

Edit the CSS variables in `jellyfin-overseerr.css`:

```css
:root {
  --jf-accent: #5b5ee1;              /* Change to your preferred accent color */
  --jf-bg: #0f111a;                  /* Change background color */
  --jf-surface: #181a25;             /* Change card background */
  /* ... more variables ... */
}
```

### Use Custom Logo

1. Add your logo file to the `assets/` folder
2. Commit and push to GitHub
3. Update the logo URL in CSS:

```css
.headerLogo {
  content: url('https://raw.githubusercontent.com/YOUR_USERNAME/jellyfin-overseerr-theme/main/assets/YOUR_LOGO.svg') !important;
}
```

### Use Custom Background

1. Add your background image (JPG, PNG, or SVG) to `assets/`
2. Update the background URL in CSS:

```css
#loginPage {
  background: url('https://raw.githubusercontent.com/YOUR_USERNAME/jellyfin-overseerr-theme/main/assets/YOUR_BACKGROUND.jpg') center/cover !important;
}
```

After making changes:
```bash
git add .
git commit -m "Customize theme colors and assets"
git push
```

Then force refresh Jellyfin (Ctrl+F5) to see changes.

---

## 🔄 Part 5: Update Theme

When you make changes to the theme:

1. Edit files locally
2. Test with `index.html`
3. Commit and push changes:
```bash
git add .
git commit -m "Description of changes"
git push
```
4. Force refresh Jellyfin (Ctrl+F5)
5. Clear browser cache if needed

---

## ⚠️ Troubleshooting

### Theme not applying?

**Solution 1**: Force refresh
- Windows/Linux: Ctrl + Shift + Delete → Clear cache
- Mac: Cmd + Shift + Delete → Clear cache

**Solution 2**: Check CSS URL
- Verify the URL is correct and accessible
- Test by pasting the URL in your browser
- Should show the raw CSS code

**Solution 3**: Check Jellyfin version
- Update to Jellyfin 10.8.0 or later
- Older versions may have CSS limitations

### Colors look wrong?

- Clear browser cache completely
- Disable browser extensions (especially dark mode extensions)
- Try a different browser to isolate the issue

### Logo not showing?

- Verify the logo URL is publicly accessible
- Check that you replaced `YOUR_GITHUB_USERNAME`
- Ensure the repository is public, not private

### Background not loading?

- Check the background file exists in `assets/`
- Verify the URL in the CSS is correct
- Try using the SVG version instead of JPG

---

## 📱 Mobile Support

The theme is fully responsive. To test on mobile:

1. Open Jellyfin on your mobile device
2. Force refresh the page
3. Navigate through different sections
4. Report any issues on GitHub

---

## 🤝 Need Help?

- **Issues**: Open an issue on GitHub
- **Questions**: Check existing issues or start a discussion
- **Contributions**: Pull requests are welcome!

---

## ✅ Checklist

Before considering setup complete:

- [ ] Repository created on GitHub
- [ ] All files pushed successfully
- [ ] URLs updated with your GitHub username
- [ ] Theme imported into Jellyfin
- [ ] Browser cache cleared
- [ ] Theme visible in Jellyfin
- [ ] Logo displaying correctly
- [ ] Background showing on login page
- [ ] Colors and gradients working
- [ ] Tested on desktop
- [ ] Tested on mobile (optional)

---

**Congratulations! Your Jellyfin Overseerr Theme is now live! 🎉**

Enjoy your beautiful new interface!

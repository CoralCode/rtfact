# 🎨 Jellyfin CSS Tips & Best Practices

Essential tips for customizing Jellyfin with CSS, based on the [official documentation](https://jellyfin.org/docs/general/clients/css-customization/).

---

## 📚 Official Resources

- **Official CSS Documentation**: https://jellyfin.org/docs/general/clients/css-customization/
- **Jellyfin Community**: https://jellyfin.org/contact/
- **CSS Reference**: https://developer.mozilla.org/en-US/docs/Web/CSS

---

## 🎯 Key Concepts

### 1. Using !important

Jellyfin uses inline styles in many places, so `!important` is **required** to override them:

```css
/* ✅ Correct - Will work */
.button {
  background: #5b5ee1 !important;
}

/* ❌ Wrong - Won't override inline styles */
.button {
  background: #5b5ee1;
}
```

### 2. CSS Comments

Use comments to organize and document your CSS:

```css
/* This is a comment - it will be ignored */

/* ============================================================
   SECTION HEADER
   ============================================================ */

.element {
  /* Inline comment explaining this property */
  color: red !important;
}
```

### 3. Color Formats

Jellyfin CSS supports multiple color formats:

```css
/* Hex Colors */
color: #5b5ee1;

/* Hex with Transparency (last 2 digits = opacity) */
background: #00000058;  /* 58 = ~35% opacity */

/* Named Colors */
color: red;
color: lightseagreen;

/* RGB/RGBA */
color: rgb(91, 94, 225);
color: rgba(91, 94, 225, 0.8);
```

**Color Tools:**
- [HTML Color Picker](https://htmlcolorcodes.com/color-picker)
- [W3Schools Color Names](https://www.w3schools.com/colors/colors_names.asp)

### 4. CSS Chaining

Apply the same style to multiple elements:

```css
/* Multiple selectors separated by commas */
.button, .emby-button, .btnPrimary {
  background: #5b5ee1 !important;
}
```

---

## 🔍 Finding Jellyfin Selectors

### Method 1: Browser DevTools (Recommended)

1. **Open DevTools**:
   - Windows/Linux: `F12` or `Ctrl + Shift + I`
   - Mac: `Cmd + Option + I`

2. **Inspect Element**:
   - Click the inspector icon (top-left of DevTools)
   - Click on the element you want to style
   - Look at the "Elements" or "Inspector" tab

3. **Find the Class/ID**:
   - Look for `class="..."` or `id="..."`
   - Common Jellyfin classes: `.button`, `.cardBox`, `.headerTabs`, etc.

### Method 2: View Page Source

1. Right-click on page → "View Page Source"
2. Search (Ctrl+F) for text near the element
3. Find the class or ID names

### Common Jellyfin Selectors

```css
/* Header & Navigation */
.skinHeader                    /* Main header */
.headerTabs                    /* Tab navigation */
.headerLogo                    /* Logo image */

/* Sidebar */
.mainDrawer                    /* Sidebar container */
.navMenuOption                 /* Menu items */

/* Buttons */
.button                        /* Generic button */
.emby-button                   /* Emby-style button */
.btnPrimary                    /* Primary button */
.paper-icon-button-light       /* Icon button */

/* Cards & Media */
.card                          /* Media card */
.cardBox                       /* Card container */
.cardContent                   /* Card content */
.cardImageContainer            /* Card image */

/* Forms */
.emby-input                    /* Text input */
.emby-textarea                 /* Textarea */
.emby-select                   /* Select dropdown */
.emby-checkbox                 /* Checkbox */

/* Dialogs */
.dialog                        /* Modal dialog */
.dialogContent                 /* Dialog content */
.dialogBackdrop                /* Dialog backdrop */

/* Pages */
#loginPage                     /* Login page */
.pageTitleContainer            /* Page title */

/* Player */
.nowPlayingBar                 /* Now playing bar */
.osdControls                   /* Video controls */
```

---

## 💡 Common Customizations

### Change Background Color

```css
body {
  background: #0f111a !important;
}
```

### Change Accent Color

```css
/* Find all accent color uses and replace */
.button-submit,
.emby-button-submit {
  background: #5b5ee1 !important;
}
```

### Add Background Image to Login

```css
#loginPage {
  background: url('YOUR_IMAGE_URL') center/cover !important;
}
```

### Make Elements Transparent

```css
.skinHeader {
  background: rgba(0, 0, 0, 0.5) !important;
  backdrop-filter: blur(10px) !important;
}
```

### Round Corners

```css
.cardContent {
  border-radius: 12px !important;
}
```

### Hide Elements

```css
/* Hide an element completely */
.elementToHide {
  display: none !important;
}
```

---

## 🎨 CSS Variables (Custom Properties)

Our theme uses CSS variables for easy customization:

```css
:root {
  --jf-accent: #5b5ee1;
  --jf-bg: #0f111a;
  --jf-radius: 12px;
}

/* Use the variables */
.button {
  background: var(--jf-accent) !important;
  border-radius: var(--jf-radius) !important;
}
```

**Benefits:**
- Change one value, update everywhere
- Easy theme customization
- Better maintainability

---

## 🔄 Testing Your Changes

### 1. Local Testing

Use the included `index.html` file:
```bash
# Open in browser
start index.html
```

### 2. Live Testing in Jellyfin

1. Paste CSS into **Dashboard → General → Custom CSS**
2. Click **Save**
3. **Force refresh** browser:
   - Windows/Linux: `Ctrl + F5`
   - Mac: `Cmd + Shift + R`

### 3. Browser DevTools Live Edit

1. Open DevTools (`F12`)
2. Go to "Elements" or "Inspector" tab
3. Edit styles in the "Styles" panel
4. See changes instantly
5. Copy working CSS to your file

---

## ⚠️ Common Issues

### Issue: CSS Not Applying

**Solutions:**
1. Add `!important` to override inline styles
2. Clear browser cache (`Ctrl + Shift + Delete`)
3. Force refresh (`Ctrl + F5`)
4. Check browser console for errors
5. Verify CSS syntax is correct

### Issue: Wrong Element Being Styled

**Solutions:**
1. Use more specific selectors
2. Check for typos in class names
3. Use browser DevTools to verify selector
4. Add parent selectors for specificity

```css
/* Less specific */
.button { }

/* More specific */
.headerTabs .button { }

/* Most specific */
.skinHeader .headerTabs .emby-button { }
```

### Issue: Colors Look Different

**Solutions:**
1. Check if browser extensions are interfering
2. Verify color format is correct
3. Test in incognito/private mode
4. Check for conflicting CSS

---

## 📏 Best Practices

### 1. Organization

```css
/* ============================================================
   SECTION NAME
   ============================================================ */

/* Subsection */
.element {
  /* Property explanation */
  property: value !important;
}
```

### 2. Naming Conventions

Use clear, descriptive names:
```css
/* ✅ Good */
--jf-accent-color
--jf-background-dark
--jf-border-radius

/* ❌ Bad */
--color1
--bg
--r
```

### 3. Comments

Add comments for:
- Section headers
- Complex selectors
- Non-obvious values
- Important notes

```css
/* ============================================================
   BUTTONS
   Styles for all button types across Jellyfin
   ============================================================ */

/* Primary action buttons with gradient */
.button-submit {
  background: linear-gradient(135deg, #5b5ee1, #8b5cf6) !important;
}
```

### 4. Specificity

Use the minimum specificity needed:
```css
/* ✅ Good - Simple and clear */
.button { }

/* ⚠️ Okay - More specific if needed */
.headerTabs .button { }

/* ❌ Bad - Overly specific */
body .layout-desktop .mainDrawer .navMenuOption .button { }
```

### 5. Performance

- Avoid overly complex selectors
- Use CSS variables for repeated values
- Minimize use of expensive properties (box-shadow, filter)
- Combine similar rules

---

## 🎓 Learning Resources

### CSS Basics
- [MDN CSS Tutorial](https://developer.mozilla.org/en-US/docs/Learn/CSS)
- [W3Schools CSS](https://www.w3schools.com/css/)
- [CSS Tricks](https://css-tricks.com/)

### CSS Variables
- [Using CSS Custom Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)

### Colors
- [HTML Color Picker](https://htmlcolorcodes.com/color-picker)
- [Color Names Reference](https://www.w3schools.com/colors/colors_names.asp)
- [Coolors - Color Palette Generator](https://coolors.co/)

### Jellyfin Specific
- [Official CSS Documentation](https://jellyfin.org/docs/general/clients/css-customization/)
- [Community Themes](https://jellyfin.org/docs/general/clients/css-customization/#community-themes)
- [Jellyfin Forums](https://forum.jellyfin.org/)

---

## 🤝 Community Themes

Learn from other Jellyfin themes:

- **[Ultrachromic](https://github.com/CTalvio/Ultrachromic)** - Extensive customization options
- **[JellySkin](https://github.com/prayag17/JellySkin)** - Vibrant with animations
- **[JellyFlix](https://github.com/prayag17/JellyFlix)** - Netflix-inspired
- **[Scyfin](https://github.com/loof2736/scyfin)** - Modern design

**Study their code to learn:**
- How they target specific elements
- Color scheme implementations
- Animation techniques
- Layout modifications

---

## 🔧 Advanced Techniques

### Gradients

```css
/* Linear gradient */
background: linear-gradient(135deg, #5b5ee1, #8b5cf6) !important;

/* Radial gradient */
background: radial-gradient(circle, #5b5ee1, #0f111a) !important;
```

### Transitions

```css
.button {
  transition: all 0.25s ease-in-out !important;
}

.button:hover {
  transform: translateY(-2px) !important;
}
```

### Backdrop Blur

```css
.skinHeader {
  backdrop-filter: blur(10px) !important;
}
```

### Box Shadows

```css
.card {
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.4) !important;
}
```

### Custom Scrollbars

```css
::-webkit-scrollbar {
  width: 12px !important;
}

::-webkit-scrollbar-thumb {
  background: #5b5ee1 !important;
  border-radius: 6px !important;
}
```

---

## 📝 Quick Reference

### Force Refresh
- **Windows/Linux**: `Ctrl + F5` or `Ctrl + Shift + R`
- **Mac**: `Cmd + Shift + R`

### Open DevTools
- **Windows/Linux**: `F12` or `Ctrl + Shift + I`
- **Mac**: `Cmd + Option + I`

### Clear Cache
- **Windows/Linux**: `Ctrl + Shift + Delete`
- **Mac**: `Cmd + Shift + Delete`

### CSS Location in Jellyfin
**Dashboard → General → Custom CSS** (scroll down)

---

## 💬 Getting Help

1. **Check the [official documentation](https://jellyfin.org/docs/general/clients/css-customization/)**
2. **Search existing GitHub issues**
3. **Ask in Jellyfin community forums**
4. **Use browser DevTools to debug**
5. **Test in incognito mode to rule out extensions**

---

**Happy theming! 🎨**

For more information, see the [official Jellyfin CSS customization documentation](https://jellyfin.org/docs/general/clients/css-customization/).

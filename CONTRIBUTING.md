# 🤝 Contributing to Jellyfin Overseerr Theme

Thank you for your interest in contributing! This document provides guidelines and instructions for contributing to the project.

---

## 📋 Table of Contents

1. [Code of Conduct](#code-of-conduct)
2. [How Can I Contribute?](#how-can-i-contribute)
3. [Development Setup](#development-setup)
4. [Coding Standards](#coding-standards)
5. [Submitting Changes](#submitting-changes)
6. [Reporting Bugs](#reporting-bugs)
7. [Suggesting Features](#suggesting-features)

---

## 📜 Code of Conduct

### Our Pledge

We are committed to providing a welcoming and inclusive environment for everyone.

### Our Standards

- ✅ Be respectful and considerate
- ✅ Welcome newcomers and help them learn
- ✅ Accept constructive criticism gracefully
- ✅ Focus on what's best for the community
- ❌ No harassment, trolling, or discriminatory behavior

---

## 🎯 How Can I Contribute?

### 1. Report Bugs 🐛

Found a bug? Help us fix it!

**Before reporting:**
- Check if the issue already exists
- Test with the latest version
- Clear browser cache and test again

**When reporting:**
- Use a clear, descriptive title
- Describe steps to reproduce
- Include screenshots if applicable
- Mention your Jellyfin version
- Specify your browser and OS

### 2. Suggest Features 💡

Have an idea? We'd love to hear it!

**Good feature suggestions:**
- Solve a real problem
- Align with the theme's goals
- Are technically feasible
- Include use cases and examples

### 3. Improve Documentation 📝

Documentation is crucial!

**You can help by:**
- Fixing typos and grammar
- Adding examples and screenshots
- Clarifying confusing sections
- Translating to other languages
- Creating video tutorials

### 4. Submit Code 🔧

Ready to code? Awesome!

**Areas to contribute:**
- Bug fixes
- New features
- Performance improvements
- Code refactoring
- Test coverage

---

## 🛠️ Development Setup

### Prerequisites

- Git
- Text editor (VS Code recommended)
- Modern web browser
- GitHub account

### Setup Steps

1. **Fork the repository**
   ```bash
   # Click "Fork" on GitHub
   ```

2. **Clone your fork**
   ```bash
   git clone https://github.com/YOUR_USERNAME/jellyfin-overseerr-theme.git
   cd jellyfin-overseerr-theme
   ```

3. **Create a branch**
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/your-bug-fix
   ```

4. **Make your changes**
   - Edit files in your favorite editor
   - Test with `index.html`
   - Verify in Jellyfin (optional but recommended)

5. **Test thoroughly**
   - Open `index.html` in multiple browsers
   - Check responsive design
   - Verify all components work
   - Test with Jellyfin if possible

---

## 📏 Coding Standards

### CSS Guidelines

**1. Use CSS Variables**
```css
/* ✅ Good */
color: var(--jf-text-primary);

/* ❌ Bad */
color: #e5e7eb;
```

**2. Add Comments**
```css
/* ✅ Good */
/* ============================================================
   BUTTONS
   ============================================================ */
.button {
  /* Primary button styles */
  background: var(--jf-accent);
}

/* ❌ Bad */
.button {
  background: var(--jf-accent);
}
```

**3. Use Consistent Naming**
```css
/* ✅ Good - Clear and descriptive */
.cardContent-button
.headerTabs
.nowPlayingBar

/* ❌ Bad - Unclear or inconsistent */
.btn
.hdr
.npb
```

**4. Maintain Structure**
```css
/* Follow this order: */
1. Positioning (position, top, left, etc.)
2. Display & Box Model (display, width, height, margin, padding)
3. Typography (font, color, text-align)
4. Visual (background, border, border-radius)
5. Misc (cursor, transition, animation)
```

**5. Use !important Sparingly**
```css
/* ✅ Good - Only when overriding Jellyfin's inline styles */
background: var(--jf-surface) !important;

/* ❌ Bad - Unnecessary use */
color: white !important;
```

### HTML Guidelines

**1. Semantic HTML**
```html
<!-- ✅ Good -->
<header>
  <nav>
    <ul>
      <li><a href="#">Home</a></li>
    </ul>
  </nav>
</header>

<!-- ❌ Bad -->
<div class="header">
  <div class="nav">
    <div class="item">Home</div>
  </div>
</div>
```

**2. Accessibility**
```html
<!-- ✅ Good -->
<button aria-label="Play video">
  <i class="icon-play"></i>
</button>

<!-- ❌ Bad -->
<div onclick="play()">
  <i class="icon-play"></i>
</div>
```

### Documentation Guidelines

**1. Clear and Concise**
- Use simple language
- Break into sections
- Add examples
- Include screenshots

**2. Keep Updated**
- Update docs with code changes
- Remove outdated information
- Add version numbers when relevant

---

## 📤 Submitting Changes

### Pull Request Process

1. **Update your branch**
   ```bash
   git fetch origin
   git rebase origin/main
   ```

2. **Commit your changes**
   ```bash
   git add .
   git commit -m "feat: add dark mode toggle"
   ```

3. **Push to your fork**
   ```bash
   git push origin feature/your-feature-name
   ```

4. **Create Pull Request**
   - Go to GitHub
   - Click "New Pull Request"
   - Fill out the template
   - Link related issues

### Commit Message Format

Use conventional commits:

```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting)
- `refactor`: Code refactoring
- `test`: Adding tests
- `chore`: Maintenance tasks

**Examples:**
```bash
feat(buttons): add gradient hover effect
fix(cards): correct border radius on mobile
docs(readme): update installation instructions
style(css): format code with prettier
refactor(variables): reorganize color palette
```

### Pull Request Template

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Code refactoring

## Testing
- [ ] Tested in Chrome
- [ ] Tested in Firefox
- [ ] Tested in Safari
- [ ] Tested on mobile
- [ ] Tested in Jellyfin

## Screenshots
Add screenshots if applicable

## Checklist
- [ ] Code follows style guidelines
- [ ] Self-review completed
- [ ] Comments added for complex code
- [ ] Documentation updated
- [ ] No new warnings generated
```

---

## 🐛 Reporting Bugs

### Bug Report Template

```markdown
**Describe the bug**
A clear description of what the bug is.

**To Reproduce**
Steps to reproduce:
1. Go to '...'
2. Click on '...'
3. See error

**Expected behavior**
What you expected to happen.

**Screenshots**
Add screenshots if applicable.

**Environment:**
- Jellyfin Version: [e.g. 10.8.0]
- Browser: [e.g. Chrome 120]
- OS: [e.g. Windows 11]
- Theme Version: [e.g. 1.0.0]

**Additional context**
Any other relevant information.
```

---

## 💡 Suggesting Features

### Feature Request Template

```markdown
**Is your feature request related to a problem?**
A clear description of the problem.

**Describe the solution you'd like**
What you want to happen.

**Describe alternatives you've considered**
Other solutions you've thought about.

**Additional context**
Mockups, examples, or references.

**Would you like to implement this?**
- [ ] Yes, I can work on this
- [ ] No, but I can help test
- [ ] No, just suggesting
```

---

## 🎨 Design Contributions

### Design Guidelines

**1. Follow Overseerr's Style**
- Dark backgrounds
- Purple-blue accents
- Rounded corners
- Clean typography

**2. Maintain Consistency**
- Use existing color palette
- Follow spacing patterns
- Match border radius
- Keep transitions smooth

**3. Consider Accessibility**
- Sufficient color contrast
- Readable font sizes
- Clear focus indicators
- Keyboard navigation support

---

## 🧪 Testing

### Testing Checklist

**Visual Testing:**
- [ ] All colors display correctly
- [ ] Gradients render smoothly
- [ ] Borders and shadows look good
- [ ] Typography is readable
- [ ] Icons are visible

**Functional Testing:**
- [ ] Buttons are clickable
- [ ] Hover effects work
- [ ] Transitions are smooth
- [ ] Forms are usable
- [ ] Navigation works

**Compatibility Testing:**
- [ ] Chrome (latest)
- [ ] Firefox (latest)
- [ ] Safari (latest)
- [ ] Edge (latest)
- [ ] Mobile browsers

**Jellyfin Testing:**
- [ ] Dashboard loads correctly
- [ ] Media cards display properly
- [ ] Player controls work
- [ ] Settings pages styled
- [ ] Login page looks good

---

## 📚 Resources

### Helpful Links

- [Jellyfin Documentation](https://jellyfin.org/docs/)
- [Overseerr GitHub](https://github.com/sct/overseerr)
- [CSS Variables Guide](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [Conventional Commits](https://www.conventionalcommits.org/)

### Learning Resources

- [CSS Tricks](https://css-tricks.com/)
- [MDN Web Docs](https://developer.mozilla.org/)
- [Web.dev](https://web.dev/)

---

## 🏆 Recognition

Contributors will be:
- Listed in CHANGELOG.md
- Mentioned in release notes
- Added to contributors list
- Credited in documentation

---

## ❓ Questions?

- **General Questions:** Open a Discussion on GitHub
- **Bug Reports:** Open an Issue
- **Feature Requests:** Open an Issue with [Feature Request] tag
- **Security Issues:** Email privately (see SECURITY.md)

---

## 📝 License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

**Thank you for contributing! 🎉**

Every contribution, no matter how small, makes this project better!

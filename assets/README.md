# Assets Folder

This folder contains the visual assets for the Jellyfin Overseerr Theme.

## Files

### logo.svg
The animated logo with purple-blue gradient and play icon. Features:
- Circular gradient ring
- Centered play button
- Subtle glow effects
- Smooth animations

### bg.svg
A dark gradient background suitable for login screens. Features:
- Purple-blue gradient spots
- Dark base (#0f111a)
- Subtle noise texture
- Animated glow effects

**Note:** You can replace `bg.svg` with `bg.jpg` or `bg.png` if you prefer to use a custom photo or image. Just update the reference in `jellyfin-overseerr.css`:

```css
#loginPage {
  background: url('https://raw.githubusercontent.com/YOUR_GITHUB_USERNAME/jellyfin-overseerr-theme/main/assets/bg.jpg') center/cover !important;
}
```

### preview.png (Optional)
Add your own screenshot of the theme in action to showcase it in the README.

## Customization

Feel free to replace any of these assets with your own:
- Use your own logo design
- Add custom background images
- Include additional graphics

Just make sure to update the URLs in the CSS file accordingly.

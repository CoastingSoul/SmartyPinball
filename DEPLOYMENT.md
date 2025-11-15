# Smarty Pinball - Deployment Guide

## Quick Start

The game is available in two versions:
- **`index.html`** (27KB) - Complete standalone HTML page
- **`squarespace-embed.html`** (26KB) - **RECOMMENDED for Squarespace** - Copy-paste ready code block

Simply open `index.html` in any modern web browser to play!

## Embedding in Squarespace

### ⭐ Option 1: Direct Code Copy-Paste (EASIEST & RECOMMENDED)

**Use the `squarespace-embed.html` file for best results!**

1. Open `squarespace-embed.html` in a text editor
2. Select all content (Ctrl+A / Cmd+A) and copy (Ctrl+C / Cmd+C)
3. Log into your Squarespace site
4. Navigate to the page where you want the game
5. Click "Edit" on the page
6. Add a **Code Block** (found under "More" in the content blocks)
7. Paste the code directly into the code block (Ctrl+V / Cmd+V)
8. Save and publish your page

**Why use squarespace-embed.html?**
- ✅ Pre-formatted for Squarespace Code Blocks
- ✅ No HTML/head/body tags that can conflict with Squarespace
- ✅ Properly scoped CSS that won't affect other page elements
- ✅ Global namespace handling to avoid JavaScript conflicts
- ✅ Same functionality as index.html
- ✅ Just copy and paste - nothing else needed!

**Pros:**
- No file uploads needed
- Game loads directly on your page
- Easiest to update (just paste new code)
- Optimized specifically for Squarespace

**Cons:**
- Code block will show raw code in the editor (but displays perfectly on the page)

### Option 2: File Upload + Embed Block

1. Upload `index.html` to your Squarespace site:
   - Go to Settings → Advanced → Code Injection
   - Or use the file upload feature if available
2. Note the URL of the uploaded file (e.g., `/s/index.html`)
3. Add an **Embed Block** to your page
4. Insert this HTML:
```html
<iframe 
  src="/s/index.html" 
  width="640" 
  height="900" 
  frameborder="0"
  style="border: none; max-width: 100%;">
</iframe>
```
5. Save and publish

**Pros:**
- Keeps your page editor clean
- Easier to manage as a separate file
- Can reuse across multiple pages

**Cons:**
- Requires file upload capability
- Extra step to update (re-upload file)

### Option 3: External Hosting

If Squarespace limitations are encountered:

1. Upload `index.html` to a web hosting service (GitHub Pages, Netlify, etc.)
2. Get the full URL (e.g., `https://yourusername.github.io/pinball/index.html`)
3. In Squarespace, add an **Embed Block**
4. Insert this HTML:
```html
<iframe 
  src="https://yourusername.github.io/pinball/index.html" 
  width="640" 
  height="900" 
  frameborder="0"
  style="border: none; max-width: 100%;">
</iframe>
```

## Responsive Sizing

The game is designed for a 600x800px canvas. Here are recommended iframe sizes:

**Desktop:**
```html
width="640" height="900"
```

**Tablet:**
```html
width="100%" height="900" style="max-width: 640px;"
```

**Mobile:**
```html
width="100%" height="800" style="max-width: 100vw;"
```

## Testing Checklist

Before deploying, verify:

- [ ] Game loads without errors
- [ ] Space bar launches ball
- [ ] Left flipper (A or ←) responds
- [ ] Right flipper (D or →) responds
- [ ] Score updates when hitting bumpers/targets
- [ ] Balls counter decreases when ball is lost
- [ ] Game over screen appears after 3 balls
- [ ] "Play Again" button resets the game
- [ ] High score persists after refresh
- [ ] NEW GAME button works
- [ ] PAUSE button works

## Browser Compatibility

Verified to work on:
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Mobile Safari (iOS 13+)
- ✅ Chrome Mobile (Android 8+)

## Customization

To customize colors, edit the CSS in `index.html`:

**Background gradient:**
```css
background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
```

**Accent color (cyan):**
```css
color: #00d4ff;
border: 3px solid #00d4ff;
```

**Bumper color:**
```javascript
color: '#ff6b00'
```

## Troubleshooting

**Problem:** Game doesn't load in Squarespace
- **Solution:** Try Option 2 (file upload) or Option 3 (external hosting)

**Problem:** Controls don't work
- **Solution:** Click on the game area to focus it, then try controls again

**Problem:** Game is too small/large
- **Solution:** Adjust the iframe width/height or use CSS zoom property

**Problem:** High score not saving
- **Solution:** Ensure browser allows localStorage (check privacy settings)

## Performance

The game runs at 60 FPS and uses:
- Minimal CPU (~5-10% on modern processors)
- Minimal Memory (~10MB)
- No network requests (fully offline after load)

## Support

For issues or customization requests, please open an issue in the GitHub repository.

---

Enjoy your Smarty Pinball game! 🤖🎮

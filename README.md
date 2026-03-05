# Frey Brightwater - Portfolio Website

A minimal, single-page portfolio website built with plain HTML, CSS, and JavaScript. No frameworks, no build tools, just clean code optimized for cheap/free hosting.

## Features

- **Responsive Design**: Mobile-first approach that works on all devices
- **Smooth Scrolling**: Seamless navigation between sections
- **Modern UI**: Clean, professional design with smooth animations
- **Accessible**: Semantic HTML, ARIA labels, keyboard navigation
- **Fast Loading**: Optimized vanilla JavaScript, no external dependencies
- **SEO Optimized**: Proper meta tags and Open Graph support

## Sections

1. **Home/Hero**: Introduction with call-to-action buttons
2. **About**: Bio and CV download link
3. **Projects**: Showcase of portfolio projects with tech stacks
4. **Skills**: Organized skill categories and tags
5. **Contact**: Email and social media links

## Local Development

### Prerequisites
- Any modern web browser (Chrome, Firefox, Safari, Edge)
- A text editor (VS Code, Sublime Text, etc.)

### Running Locally

1. **Clone or download** this repository to your computer

2. **Open in browser**:
   - Simply double-click `index.html`, or
   - Right-click `index.html` → Open with → Your browser

3. **For local server** (optional, for better testing):
   ```bash
   # Using Python 3
   python -m http.server 8000

   # Using Python 2
   python -m SimpleHTTPServer 8000

   # Using Node.js (install http-server globally first)
   npx http-server
   ```
   Then visit `http://localhost:8000`

## Customization Guide

### Update Your Information

1. **Personal Details** (`index.html`):
   - Line 13-16: Update meta tags
   - Line 18: Change title
   - Line 35: Update hero title and subtitle
   - Line 52-60: Edit about section bio
   - Line 162-171: Update contact email and social links

2. **Projects** (`index.html`, lines 70-150):
   - Replace placeholder projects with your actual work
   - Update project titles, descriptions, and tech stacks
   - Add real GitHub and live demo links

3. **Skills** (`index.html`, lines 154-185):
   - Modify skill tags to match your expertise
   - Add or remove skill categories as needed

4. **CV/Resume**:
   - Replace `FreyBrightwater_CV.pdf` with your own PDF
   - Update the link on line 64 if you rename the file

### Styling Changes

**Colors** (`styles.css`, lines 5-18):
```css
--primary-color: #2563eb;    /* Main brand color */
--primary-dark: #1e40af;     /* Hover states */
--text-color: #1e293b;       /* Main text */
--bg-color: #ffffff;         /* Background */
```

**Fonts** (`styles.css`, line 23):
```css
--font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', ...;
```

**Hero Background** (`styles.css`, line 245):
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Adding New Sections

1. Add section HTML in `index.html`:
```html
<section id="new-section" class="section">
    <div class="container">
        <h2 class="section-title">New Section</h2>
        <!-- Your content here -->
    </div>
</section>
```

2. Add navigation link:
```html
<li class="nav-item"><a href="#new-section" class="nav-link">New Section</a></li>
```

3. Style in `styles.css` if needed

## Deployment Options

### Recommended: Netlify (Easiest)

**Cost**: FREE
**Best for**: Beginners, drag-and-drop deployment

1. Go to [netlify.com](https://www.netlify.com/)
2. Sign up for free account
3. Drag and drop your entire `Website` folder onto Netlify
4. Done! Your site is live with HTTPS

**Bonus**: Get a free `yourname.netlify.app` subdomain, or connect a custom domain

### GitHub Pages

**Cost**: FREE
**Best for**: Developers familiar with Git

1. Create a GitHub account at [github.com](https://github.com)
2. Create a new repository named `your-username.github.io`
3. Upload all files (index.html, styles.css, script.js, PDF)
4. Go to Settings → Pages → Select main branch → Save
5. Your site will be live at `https://your-username.github.io`

**Commands**:
```bash
git init
git add .
git commit -m "Initial portfolio commit"
git branch -M main
git remote add origin https://github.com/your-username/your-username.github.io.git
git push -u origin main
```

### Vercel

**Cost**: FREE
**Best for**: Fast deployment with Git integration

1. Go to [vercel.com](https://vercel.com)
2. Sign up with GitHub
3. Import your repository or drag & drop files
4. Deploy automatically

### Cloudflare Pages

**Cost**: FREE (Unlimited bandwidth!)
**Best for**: High-traffic sites

1. Go to [pages.cloudflare.com](https://pages.cloudflare.com)
2. Sign up for free
3. Connect GitHub repo or upload files
4. Deploy with unlimited bandwidth

### Firebase Hosting

**Cost**: FREE (10GB storage, 360MB/day transfer)
**Best for**: Those using other Google services

1. Install Firebase CLI: `npm install -g firebase-tools`
2. Login: `firebase login`
3. Initialize: `firebase init hosting`
4. Deploy: `firebase deploy`

## Hosting Comparison

| Platform | Cost | Bandwidth | HTTPS | Custom Domain | Deployment |
|----------|------|-----------|-------|---------------|------------|
| **Netlify** | Free | 100GB/mo | ✅ | ✅ | Drag & drop |
| **GitHub Pages** | Free | Soft limit | ✅ | ✅ | Git push |
| **Vercel** | Free | 100GB/mo | ✅ | ✅ | Git / CLI |
| **Cloudflare Pages** | Free | Unlimited | ✅ | ✅ | Git |
| **Firebase** | Free | 10GB/mo | ✅ | ✅ | CLI |

### Custom Domain (Optional)

**Where to buy**: Namecheap, Porkbun, Cloudflare (~$10-15/year)

All free hosting platforms above support custom domains at no extra cost!

## File Structure

```
Website/
├── index.html              # Main HTML structure
├── styles.css             # All styling
├── script.js              # Interactivity & animations
├── FreyBrightwater_CV.pdf # Your CV/resume
└── README.md              # This file
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance

- **No external dependencies**: Zero HTTP requests to CDNs
- **Optimized images**: Use WebP format when possible
- **Minify for production** (optional):
  ```bash
  # CSS minification online: https://cssminifier.com/
  # JS minification online: https://javascript-minifier.com/
  ```

## Accessibility Features

- Semantic HTML5 elements
- ARIA labels for screen readers
- Keyboard navigation support
- Sufficient color contrast
- Responsive text sizing

## SEO Checklist

- ✅ Descriptive page title
- ✅ Meta description
- ✅ Open Graph tags for social sharing
- ✅ Semantic HTML structure
- ✅ Fast loading time
- ✅ Mobile-friendly
- ✅ HTTPS (via hosting platform)

## Troubleshooting

**CV link not working?**
- Ensure `FreyBrightwater_CV.pdf` is in the same folder as `index.html`
- Check file name matches exactly (case-sensitive)

**Mobile menu not opening?**
- Check JavaScript console for errors (F12 in browser)
- Ensure `script.js` is loaded correctly

**Styles not applying?**
- Clear browser cache (Ctrl+Shift+R or Cmd+Shift+R)
- Check `styles.css` is linked correctly in `index.html`

**Smooth scrolling not working?**
- Some older browsers don't support smooth scrolling
- JavaScript fallback is included in `script.js`

## Next Steps

1. ✅ Customize content with your information
2. ✅ Replace placeholder projects with real work
3. ✅ Update CV/resume PDF
4. ✅ Choose a hosting platform
5. ✅ Deploy your site
6. ✅ (Optional) Purchase and connect custom domain
7. ✅ Share your portfolio!

## Support

Need help? Here are some resources:
- [MDN Web Docs](https://developer.mozilla.org/) - HTML/CSS/JS reference
- [Stack Overflow](https://stackoverflow.com/) - Community Q&A
- [Web.dev](https://web.dev/) - Best practices and guides

## License

This template is free to use for personal and commercial projects.

---

**Built with ❤️ using plain HTML, CSS, and JavaScript**

*No frameworks. No build tools. No complexity. Just clean code.*

# Quick Start Guide

This guide will help you get your personal website up and running in minutes.

## ⚡ Quick Setup (5 minutes)

### 1. Install Dependencies

```bash
npm install
```

### 2. Start Development Server

```bash
npm run dev
```

Your site will be available at `http://localhost:4321`

### 3. Customize Content

#### Add Your Photo
Place your professional headshot at:
```
public/images/profile.jpg
```
Recommended size: 400x400px or larger (square aspect ratio)

#### Update Personal Information

Edit `src/pages/index.astro` to update:
- Your name and tagline
- Professional summary
- Current positions
- Recent research highlights

#### Update Research Projects

Edit `src/pages/research.astro` to:
- Add/remove research projects
- Update project descriptions
- Add collaborators and links

#### Update Teaching

Edit `src/pages/teaching.astro` to:
- Add your courses
- Update teaching philosophy
- Add student projects

#### Update Publications

Edit `src/pages/publications.astro` to:
- Add your papers
- Update talks and presentations
- Add media appearances

#### Update Projects/Initiatives

Edit `src/pages/projects.astro` to:
- Showcase your leadership roles
- Update initiative descriptions
- Add impact metrics

### 4. Customize Appearance

#### Change Colors

Edit `public/styles/global.css` and modify the CSS variables:

```css
:root {
  --color-accent: #8b2635;        /* Change to your preferred color */
}
```

#### Change Fonts

Update the Google Fonts link in `src/layouts/BaseLayout.astro` and CSS variables in `global.css`

### 5. Deploy to GitHub Pages

#### First Time Setup

1. Go to your GitHub repository settings
2. Navigate to "Pages" (under Code and automation)
3. Under "Source", select "GitHub Actions"

#### Push Your Changes

```bash
git add .
git commit -m "Customize personal website"
git push origin main
```

The GitHub Action will automatically build and deploy your site!

Your site will be live at: `https://YOUR-USERNAME.github.io`

## 📝 Content Guidelines

### Profile Photo
- Use a professional headshot
- Square aspect ratio (1:1)
- Good lighting
- Neutral or professional background
- File size: < 500KB for fast loading

### Writing Style
- **First Person**: Use "I" and "my"
- **Concise**: Clear and to the point
- **Professional**: Academic yet approachable
- **Specific**: Include dates, metrics, and concrete details

### Research Projects
For each project, include:
- Clear title and tags
- Brief overview (2-3 sentences)
- Key innovations or contributions
- Collaborators and status
- Links to code/papers when available

### Publications
Use this format:
```
Title of Paper
Authors (highlight your name)
Venue, Year
[PDF] • [BibTeX] • [Code]
```

## 🎨 Customization Tips

### Adding a New Section

1. Add a new `<section>` in the relevant `.astro` file:
```astro
<section id="new-section">
  <h2 class="section-title">New Section</h2>
  <p>Your content here...</p>
</section>
```

2. Add navigation link in `src/layouts/BaseLayout.astro`:
```astro
<a href="#new-section">New Section</a>
```

### Creating a New Page

1. Create `src/pages/new-page.astro`:
```astro
---
import BaseLayout from '../layouts/BaseLayout.astro';
---

<BaseLayout title="New Page">
  <h1>New Page</h1>
  <p>Content goes here...</p>
</BaseLayout>
```

2. Add to navigation in `BaseLayout.astro`

### Styling Cards

Use the existing card styles:
```astro
<div class="card">
  <h3>Card Title</h3>
  <p>Card description...</p>
  <div class="card-tags">
    <span class="tag">Tag1</span>
    <span class="tag">Tag2</span>
  </div>
</div>
```

## 🔧 Common Tasks

### Update Contact Information

Edit the footer section in `src/layouts/BaseLayout.astro`

### Change Social Media Links

Update the social links in the footer of `src/layouts/BaseLayout.astro`

### Add Google Analytics

Add to `<head>` in `src/layouts/BaseLayout.astro`:
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR-GA-ID"></script>
<script is:inline>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'YOUR-GA-ID');
</script>
```

### Change Default Theme

To set dark mode as default, change in `src/layouts/BaseLayout.astro`:
```javascript
if (localStorage.theme === 'light' || (!('theme' in localStorage) && window.matchMedia('(prefers-color-scheme: light)').matches)) {
  document.documentElement.classList.remove('dark')
} else {
  document.documentElement.classList.add('dark')
}
```

## 🐛 Troubleshooting

### Build Fails
- Check Node.js version: `node --version` (should be 18.17.1+)
- Clear cache: `rm -rf node_modules package-lock.json && npm install`
- Check for syntax errors in `.astro` files

### Styles Not Updating
- Hard refresh browser: Ctrl+Shift+R (or Cmd+Shift+R on Mac)
- Clear browser cache
- Restart dev server

### Images Not Loading
- Ensure images are in `public/images/`
- Use absolute paths: `/images/photo.jpg` (not `../images/photo.jpg`)
- Check file extensions match (case-sensitive)

### Dark Mode Not Working
- Clear localStorage: Open browser console and run `localStorage.clear()`
- Check browser console for JavaScript errors

## 📚 Further Reading

- [Astro Documentation](https://docs.astro.build)
- [Markdown Guide](https://www.markdownguide.org/)
- [CSS Variables (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [GitHub Pages Docs](https://docs.github.com/en/pages)

## 💡 Tips for Maintenance

### Regular Updates
- Update research projects when published
- Add new publications immediately
- Update teaching materials each semester
- Keep news/updates section current (last 6-12 months)

### Version Control
- Commit changes regularly
- Use descriptive commit messages
- Create branches for major redesigns

### Performance
- Optimize images before uploading (use tools like TinyPNG)
- Keep page sizes reasonable (< 1MB)
- Minimize external dependencies

### SEO
- Update page titles and descriptions
- Use descriptive headings (H1, H2, H3)
- Add alt text to all images
- Keep URLs clean and meaningful

## 🆘 Need Help?

- Check the main [README.md](README.md) for detailed documentation
- Review the [Astro documentation](https://docs.astro.build)
- Open an issue on GitHub if you find bugs
- Email: venkat.eduseva@gmail.com

---

Happy building! 🚀

**विद्यया अमृतमश्नुते**


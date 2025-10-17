# Dr. Venkatapathy Subramanian - Personal Website

A clean, elegant, and intellectually grounded personal website showcasing research, teaching, and transdisciplinary initiatives at the intersection of Artificial Intelligence and Indian Knowledge Systems.

🌐 **Live Site:** [venkatapathy.github.io](https://venkatapathy.github.io)

## 🎨 Design Philosophy

This website embodies a minimalist, modern aesthetic with:

- **Clean Layout:** White background with muted wine/indigo accent colors
- **Typography:** IBM Plex Serif for body text, Inter for headers
- **Cultural Elements:** Subtle Sanskrit quotes and Indic design cues
- **Dark Mode:** Seamless light/dark theme toggle
- **Responsive:** Mobile-first design that works beautifully on all devices

Inspired by academic personal sites like [karpathy.github.io](https://karpathy.github.io) and [yoshuabengio.org](https://yoshuabengio.org).

## 🏗️ Tech Stack

- **Framework:** [Astro](https://astro.build) - Modern static site generator
- **Styling:** Custom CSS with CSS Variables for theming
- **Deployment:** GitHub Pages with automatic deployment via GitHub Actions
- **Fonts:** Google Fonts (IBM Plex Serif, Inter)

## 📂 Project Structure

```
venkatapathy.github.io/
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions deployment
├── content/                    # Markdown content files
│   ├── about/
│   ├── research/
│   ├── teaching/
│   ├── publications/
│   └── projects/
├── public/
│   ├── images/                 # Images and assets
│   └── styles/
│       └── global.css          # Global styles
├── src/
│   ├── components/             # Reusable components
│   ├── layouts/
│   │   └── BaseLayout.astro    # Main layout template
│   └── pages/                  # Page routes
│       ├── index.astro         # Homepage
│       ├── research.astro
│       ├── teaching.astro
│       ├── publications.astro
│       └── projects.astro
├── astro.config.mjs            # Astro configuration
├── package.json
├── tsconfig.json
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- Node.js 18.20.8 or higher (or Node.js 20.3.0+, 22.0.0+)
- npm or yarn

### Local Development

1. **Clone the repository:**
   ```bash
   git clone https://github.com/venkatapathy/venkatapathy.github.io.git
   cd venkatapathy.github.io
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Start the development server:**
   ```bash
   npm run dev
   ```

4. **Open your browser:**
   Navigate to `http://localhost:4321`

The site will automatically reload when you make changes.

### Building for Production

```bash
npm run build
```

This generates a static site in the `dist/` directory.

### Preview Production Build

```bash
npm run preview
```

## 📝 Updating Content

### Adding/Editing Pages

All main pages are in `src/pages/`. To edit content:

1. Open the relevant `.astro` file (e.g., `src/pages/research.astro`)
2. Edit the HTML/content within the file
3. Save and the dev server will hot-reload

### Changing Styles

- **Global styles:** Edit `public/styles/global.css`
- **Component-specific styles:** Add `<style>` blocks in `.astro` files
- **Theme colors:** Modify CSS variables in `:root` (light mode) and `.dark` (dark mode)

### Adding Images

1. Place images in `public/images/`
2. Reference them in your pages as `/images/your-image.jpg`
3. For profile photo: Add as `/images/profile.jpg`

### Updating Research/Publications

Edit the content directly in the respective `.astro` files:
- Research: `src/pages/research.astro`
- Publications: `src/pages/publications.astro`

## 🌙 Dark Mode

Dark mode is implemented with:
- CSS variables for all colors
- JavaScript to toggle the `dark` class on `<html>`
- Local storage to persist user preference
- Respects system preference on first visit

## 🚢 Deployment

The site automatically deploys to GitHub Pages when you push to the `main` branch.

### First-Time Setup

1. **Enable GitHub Pages:**
   - Go to your repository Settings
   - Navigate to Pages (under Code and automation)
   - Set Source to "GitHub Actions"

2. **Push to main branch:**
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

3. **Wait for deployment:**
   - Check the "Actions" tab in your GitHub repository
   - Once the workflow completes, your site will be live!

### Manual Deployment

If you need to manually trigger deployment:
1. Go to the "Actions" tab in your repository
2. Select "Deploy to GitHub Pages" workflow
3. Click "Run workflow"

## 📄 Content Guidelines

### Writing Style
- **Academic yet accessible:** Clear, precise language
- **First person:** Use "I" and "my" for a personal touch
- **Active voice:** Preferred over passive constructions
- **Brevity:** Be concise while being comprehensive

### Sections to Maintain
- **About:** Professional summary, current roles, focus areas
- **Research:** Detailed project descriptions with collaborators
- **Teaching:** Course listings, teaching philosophy
- **Publications:** Papers, talks, media appearances
- **Projects:** Leadership roles, initiatives, impact metrics

## 🎨 Customization

### Changing Accent Color

Edit the CSS variables in `public/styles/global.css`:

```css
:root {
  --color-accent: #8b2635;        /* Your primary accent color */
  --color-accent-hover: #6d1e2a;  /* Darker shade for hover states */
}

.dark {
  --color-accent: #c94857;        /* Accent for dark mode */
  --color-accent-hover: #e05565;
}
```

### Fonts

To change fonts, update the Google Fonts import in `src/layouts/BaseLayout.astro` and the CSS variables:

```css
--font-serif: 'IBM Plex Serif', Georgia, serif;
--font-sans: 'Inter', sans-serif;
```

## 📱 Responsive Design

The site is fully responsive with breakpoints at:
- **Desktop:** 1200px+
- **Tablet:** 768px - 1199px
- **Mobile:** < 768px

Mobile navigation is simplified to show only essential links.

## ♿ Accessibility

- Semantic HTML throughout
- ARIA labels on interactive elements
- Keyboard navigation support
- Color contrast ratios meet WCAG AA standards
- Focus indicators for keyboard users

## 📊 SEO

- Unique meta titles and descriptions for each page
- Semantic HTML structure
- Clean URLs
- Fast load times (static site)
- Sitemap automatically generated by Astro

## 🤝 Contributing

This is a personal website, but if you notice any issues or have suggestions:

1. Open an issue describing the problem or suggestion
2. For bugs, include steps to reproduce
3. For enhancements, explain the benefit

## 📜 License

- **Content:** © 2025 Dr. Venkatapathy Subramanian. Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
- **Code:** MIT License (see LICENSE file)

## 🙏 Acknowledgments

- Design inspired by [Andrej Karpathy](https://karpathy.github.io) and [Yoshua Bengio](https://yoshuabengio.org)
- Built with [Astro](https://astro.build)
- Fonts from [Google Fonts](https://fonts.google.com)
- Icons from [Lucide](https://lucide.dev)

## 📧 Contact

- **Email:** venkat.eduseva@gmail.com
- **GitHub:** [@venkatapathy](https://github.com/venkatapathy)
- **Twitter/X:** [@AnaadiAI](https://twitter.com/AnaadiAI)
- **LinkedIn:** [venkatapathy-subramanian](https://www.linkedin.com/in/venkatapathy-subramanian)

---

**विद्यया अमृतमश्नुते** — *Through knowledge one attains immortality*

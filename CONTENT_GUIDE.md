# Content Management Guide

This guide provides detailed instructions for managing and updating content on your personal website.

## 📁 Content Organization

### File Structure
```
src/pages/
├── index.astro          # Homepage (About section)
├── research.astro       # Research projects
├── teaching.astro       # Teaching philosophy & courses
├── publications.astro   # Papers, talks, media
└── projects.astro       # Initiatives & leadership

content/                 # Optional: Markdown files for future use
├── about/
├── research/
├── teaching/
├── publications/
└── projects/

public/
├── images/              # All images
└── styles/
    └── global.css       # Styling
```

## 🏠 Homepage (index.astro)

### Hero Section
```astro
<div class="hero">
  <div class="hero-content">
    <div class="hero-text">
      <h1>Your Name</h1>
      <p class="tagline">Your Title/Focus Area</p>
      <p>
        Your professional summary (2-3 sentences)...
      </p>
    </div>
    <img src="/images/profile.jpg" alt="Your Name" class="hero-image" />
  </div>
</div>
```

**Tips:**
- Keep tagline concise (under 10 words)
- Professional summary should capture your unique position
- Profile photo should be professional, well-lit, square aspect ratio

### Sanskrit Quote
```astro
<div class="sanskrit-quote">
  Sanskrit text — English translation
</div>
```

You can use Unicode for Devanagari text or romanized Sanskrit.

### About Section
Structure:
1. Current position(s)
2. Educational background
3. Current focus areas (bulleted list)
4. Selected positions (bulleted list)

### Recent Research Highlights
Display 3-4 key projects as cards:
```astro
<div class="card">
  <h3>Project Name</h3>
  <p>Brief description (2-3 sentences)</p>
  <div class="card-tags">
    <span class="tag">Tag1</span>
    <span class="tag">Tag2</span>
  </div>
</div>
```

## 🔬 Research Page (research.astro)

### Project Structure
```astro
<div class="project">
  <h3>Project Title</h3>
  <div class="card-tags">
    <span class="tag">Category</span>
  </div>
  
  <p><strong>Overview:</strong> Project description...</p>
  
  <p><strong>Key Features/Innovations:</strong></p>
  <ul>
    <li>Feature 1</li>
    <li>Feature 2</li>
  </ul>
  
  <p>
    <strong>Collaborators:</strong> Names<br>
    <strong>Status:</strong> Active/Completed | <a href="#">Link</a>
  </p>
</div>
```

### Research Interests Cards
Use 3-6 cards highlighting your broad research areas:
```astro
<div class="card">
  <h3>Research Area</h3>
  <p>Brief description of this research interest</p>
</div>
```

### Tags
Consistent tags help visitors understand your work:
- **Languages:** Tamil, Sanskrit, Hindi, etc.
- **Technologies:** NLP, ML, OCR, Knowledge Graphs, etc.
- **Domains:** IKS, Digital Humanities, Healthcare, Education, etc.

## 👨‍🏫 Teaching Page (teaching.astro)

### Teaching Philosophy
Start with a personal statement (2-3 paragraphs):
- Your approach to teaching
- What you emphasize
- Cultural/philosophical influences

### Course Structure
```astro
<div class="course">
  <h3>Course Name</h3>
  <div class="course-meta">
    <span>Level</span> • <span>Duration</span> • <span>Semester/Year</span>
  </div>
  
  <p>Course description...</p>
  
  <p><strong>Topics Covered:</strong></p>
  <ul>
    <li>Topic 1</li>
    <li>Topic 2</li>
  </ul>
  
  <p><strong>Projects:</strong> Description of course projects</p>
</div>
```

### Course Levels
- **Undergraduate:** For bachelor's students
- **Graduate:** For master's/PhD students
- **Graduate/Advanced Undergraduate:** Mixed level
- **Workshop Series:** Short intensive courses

## 📄 Publications Page (publications.astro)

### Publication Item Structure
```astro
<li class="publication-item">
  <div class="publication-title">
    Paper Title in Sentence Case
  </div>
  <div class="publication-authors">
    First Author, Second Author, Your Name, Last Author
  </div>
  <div class="publication-venue">
    Conference/Journal Name, Year
  </div>
  <div class="publication-links">
    <a href="#">PDF</a> • <a href="#">BibTeX</a> • <a href="#">Code</a>
  </div>
</li>
```

### Sections
Organize publications into:
1. **Journal Papers** - Peer-reviewed journal publications
2. **Conference Papers** - Full conference papers
3. **Workshop Papers & Extended Abstracts** - Shorter works
4. **Invited Talks & Presentations** - Speaking engagements
5. **Thesis** - Dissertation/thesis
6. **Media & Outreach** - Popular articles, interviews

### Author Name Formatting
You can bold your name in author lists:
```astro
<div class="publication-authors">
  A. Kumar, <strong>V. Subramanian</strong>, R. Krishnan
</div>
```

### Talk Structure
```astro
<li class="talk-item">
  <div class="talk-title">Talk Title</div>
  <div class="talk-venue">Venue - Date</div>
  <div class="publication-links"><a href="#">Video</a> • <a href="#">Slides</a></div>
</li>
```

## 🌟 Projects Page (projects.astro)

### Featured Project Structure
```astro
<div class="featured-project">
  <div class="project-header">
    <div>
      <h3>Your Role</h3>
      <div class="project-meta">Dates • Location</div>
    </div>
    <div class="project-logo">
      <img src="/images/logo.png" alt="Project Name" />
    </div>
  </div>
  
  <p>Project description...</p>
  
  <h4>Mission</h4>
  <p>Mission statement...</p>
  
  <h4>Key Programs</h4>
  <div class="program">
    <h5>Program Name</h5>
    <p>Description...</p>
    <ul>
      <li>Feature/achievement</li>
    </ul>
  </div>
  
  <h4>Impact</h4>
  <ul>
    <li><strong>Metric:</strong> Description</li>
  </ul>
</div>
```

### Initiative Cards
For smaller initiatives:
```astro
<div class="initiative-card">
  <h3>Initiative Name</h3>
  <p class="role">Your Role</p>
  <p>Description...</p>
</div>
```

## 🎨 Styling Guidelines

### Headings Hierarchy
- **H1:** Page title (only one per page)
- **H2:** Major section titles
- **H3:** Subsection titles or card titles
- **H4:** Within sections for organization
- **H5:** Lowest level, use sparingly

### Lists
**Bulleted lists** for:
- Features
- Topics
- Items without order

**Numbered lists** for:
- Steps in a process
- Chronological items
- Ranked items

### Emphasis
- **Bold (`<strong>`):** Important terms, labels, metrics
- *Italic (`<em>`):** Titles of works, foreign words
- `Code formatting:` Technical terms, file names

### Links
Internal links (within site):
```astro
<a href="/research">Research</a>
<a href="#section-id">Jump to section</a>
```

External links (add target="_blank"):
```astro
<a href="https://example.com" target="_blank" rel="noopener noreferrer">External</a>
```

## 🏷️ Tags and Categories

### Recommended Tags

**Technology:**
- AI, ML, NLP, OCR, Computer Vision
- LLM, SLM, Knowledge Graphs
- Deep Learning, Reinforcement Learning

**Languages:**
- Tamil, Sanskrit, Hindi, Telugu, etc.
- Indic Languages, Dravidian, Indo-Aryan

**Domains:**
- IKS, Digital Humanities, Education
- Healthcare, Agriculture, Rural Development
- Ayurveda, Astronomy, Mathematics

**Status/Type:**
- Open Source, Research, Active Development
- Completed, In Progress, Pilot Phase

## 📸 Image Guidelines

### Profile Photo
- **Format:** JPG or PNG
- **Size:** 400x400px minimum (1:1 aspect ratio)
- **File size:** < 300KB
- **Quality:** Professional, good lighting
- **Location:** `public/images/profile.jpg`

### Project Logos
- **Format:** PNG with transparency preferred
- **Size:** Max 200px width
- **File size:** < 100KB
- **Location:** `public/images/project-name-logo.png`

### Content Images
- **Format:** JPG for photos, PNG for graphics
- **Max width:** 1200px
- **File size:** < 500KB per image
- **Alt text:** Always include descriptive alt text

### Optimization
Use tools like:
- [TinyPNG](https://tinypng.com) - Compress images
- [Squoosh](https://squoosh.app) - Advanced compression
- ImageMagick (command line) - Batch processing

## 📝 Writing Best Practices

### Academic Style
- Clear, concise sentences
- Active voice preferred
- First person ("I", "my") for personal site
- Professional but approachable tone

### Length Guidelines
- **Tagline:** 5-10 words
- **Card description:** 2-3 sentences
- **Project overview:** 3-5 sentences
- **Full project description:** 2-3 paragraphs
- **Teaching philosophy:** 2-4 paragraphs

### Keywords
Include relevant keywords naturally for SEO:
- Your name
- Research areas
- Technologies you work with
- Locations/institutions

### Dates
Be consistent with date formatting:
- **Publications:** "2024" or "January 2024"
- **Projects:** "2020 - Present" or "2019 - 2023"
- **Events:** "October 2023" or "Oct 2023"

## 🔄 Regular Maintenance

### Monthly
- [ ] Add new publications
- [ ] Update news/recent updates section
- [ ] Check all external links

### Semester/Annually
- [ ] Update teaching courses
- [ ] Refresh research project status
- [ ] Update metrics (students trained, papers published, etc.)
- [ ] Archive old news items

### As Needed
- [ ] Add new research projects when started
- [ ] Update positions/affiliations
- [ ] Add talks and presentations
- [ ] Update profile photo

## 🌐 Multilingual Content

### Adding Tamil/Sanskrit Text
Use Unicode directly in Astro files:
```astro
<p class="tamil">தமிழ் உரை</p>
<p class="sanskrit">संस्कृत पाठः</p>
```

Add custom styling in `global.css`:
```css
.tamil {
  font-family: 'Noto Sans Tamil', sans-serif;
  font-size: 1.1em;
}
```

### Transliteration
For romanized Sanskrit/Tamil:
```astro
<p class="transliteration">vidyayā amṛtamaśnute</p>
```

## 📱 Mobile Considerations

### Content Length
- Keep paragraphs shorter for mobile readability
- Use subheadings to break up long sections
- Cards should be scannable

### Images
- Test image loading on mobile
- Ensure text in images is readable at small sizes
- Avoid horizontal scrolling

## ♿ Accessibility

### Alt Text
Every image needs descriptive alt text:
```astro
<img src="/images/chart.jpg" alt="Bar chart showing increase in student enrollment from 2020 to 2024">
```

### Link Text
Use descriptive link text:
- ✅ "Read the full paper on neural tokenization"
- ❌ "Click here" or "Read more"

### Headings
- Don't skip heading levels (H2 → H3 → H4)
- Use headings for structure, not just styling
- One H1 per page

## 🔍 SEO Tips

### Page Titles
Format: "Specific Topic - Your Name"
```astro
<BaseLayout title="Research - Dr. Venkatapathy Subramanian">
```

### Meta Descriptions
Write unique descriptions for each page (155-160 characters):
```astro
<BaseLayout 
  title="Research"
  description="Research projects exploring AI and Indian Knowledge Systems..."
>
```

### Internal Linking
Link related pages/sections:
- From homepage to detailed pages
- From research to relevant publications
- From projects to related research

## 🎯 Call-to-Action

Include clear CTAs where appropriate:
```astro
<p class="cta">
  Interested in collaboration? <a href="/#contact">Get in touch →</a>
</p>
```

Use cases:
- End of research projects (for collaboration)
- After publications (to cite or discuss)
- Teaching page (for prospective students)

---

## 💡 Pro Tips

1. **Consistency is key** - Use consistent formatting, voice, and style
2. **Update regularly** - Fresh content helps with SEO and shows activity
3. **Show, don't just tell** - Include metrics, examples, and concrete details
4. **Balance depth and brevity** - Detailed enough to inform, concise enough to read
5. **Make it personal** - This is YOUR site - let your personality show through
6. **Test on mobile** - Most visitors will view on phones
7. **Get feedback** - Ask colleagues to review before publishing
8. **Version control** - Commit changes with clear messages

---

Need help? Check [README.md](README.md) or [QUICKSTART.md](QUICKSTART.md) for more information.


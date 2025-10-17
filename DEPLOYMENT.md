# Deployment Checklist

Follow this checklist before deploying your website to ensure everything is ready for production.

## 🎯 Pre-Deployment Checklist

### Content Review

- [ ] **Profile photo** added at `public/images/profile.jpg`
- [ ] **Personal information** updated on homepage
- [ ] **Contact details** verified (email, phone, social media links)
- [ ] **Research projects** descriptions completed
- [ ] **Publications** list is current and accurate
- [ ] **Teaching** courses and philosophy updated
- [ ] **Projects/Initiatives** accurately described
- [ ] **Sanskrit quotes** and cultural elements verified
- [ ] All **placeholder text** removed or replaced
- [ ] All **"Lorem ipsum"** text removed

### Technical Review

- [ ] Site **builds successfully** (`npm run build`)
- [ ] All **internal links** work correctly
- [ ] All **external links** tested and working
- [ ] **Images load** properly on all pages
- [ ] **Dark mode** toggle works on all pages
- [ ] Site is **responsive** on mobile, tablet, and desktop
- [ ] **Navigation** works smoothly
- [ ] **Contact section** in footer is complete
- [ ] No **console errors** in browser developer tools
- [ ] **Page load time** is acceptable (< 3 seconds)

### SEO & Metadata

- [ ] Each page has unique **title**
- [ ] Each page has unique **meta description**
- [ ] **Favicon** added (optional but recommended)
- [ ] **Open Graph tags** added for social sharing (optional)
- [ ] **robots.txt** configured (if needed)
- [ ] **Sitemap** generated (Astro does this automatically)

### Accessibility

- [ ] All images have **alt text**
- [ ] **Heading hierarchy** is correct (H1 → H2 → H3)
- [ ] **Link text** is descriptive (no "click here")
- [ ] **Color contrast** meets WCAG AA standards
- [ ] Site is **keyboard navigable**
- [ ] **ARIA labels** on interactive elements

### GitHub Repository

- [ ] Repository is **public** (for GitHub Pages)
- [ ] **README.md** is complete and helpful
- [ ] **.gitignore** is properly configured
- [ ] No **sensitive information** (API keys, passwords) in code
- [ ] **package.json** has correct information
- [ ] **License** file is present

## 🚀 Deployment Steps

### 1. Final Local Build

```bash
# Clean install
rm -rf node_modules package-lock.json
npm install

# Build
npm run build

# Preview production build
npm run preview
```

Visit `http://localhost:4321` and thoroughly test the production build.

### 2. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings**
3. Click **Pages** (in the sidebar under "Code and automation")
4. Under **Source**, select **GitHub Actions**
5. Save the settings

### 3. Commit and Push

```bash
# Add all changes
git add .

# Commit with descriptive message
git commit -m "Initial website deployment"

# Push to main branch
git push origin main
```

### 4. Monitor Deployment

1. Go to the **Actions** tab in your GitHub repository
2. Watch the "Deploy to GitHub Pages" workflow
3. Wait for the green checkmark (usually 2-3 minutes)
4. Check for any errors in the workflow logs

### 5. Verify Live Site

1. Visit `https://YOUR-USERNAME.github.io`
2. Test all pages and navigation
3. Check dark mode toggle
4. Test responsive design (mobile, tablet, desktop)
5. Verify all links work
6. Check images load correctly

## 🔍 Post-Deployment Testing

### Browser Testing

Test on multiple browsers:
- [ ] **Chrome** (desktop & mobile)
- [ ] **Firefox** (desktop & mobile)
- [ ] **Safari** (desktop & iOS)
- [ ] **Edge** (desktop)

### Device Testing

- [ ] **Desktop** (1920x1080 and higher)
- [ ] **Laptop** (1366x768)
- [ ] **Tablet** (iPad, 768x1024)
- [ ] **Mobile** (iPhone, Android, various sizes)

### Functionality Testing

- [ ] Navigation menu works
- [ ] All page links function
- [ ] Dark mode toggle works
- [ ] Smooth scrolling to anchors works
- [ ] External links open in new tabs
- [ ] Contact information is clickable (email, phone)
- [ ] Social media icons link correctly

### Performance Testing

Use [Google PageSpeed Insights](https://pagespeed.web.dev/):
- [ ] **Mobile score** > 90
- [ ] **Desktop score** > 95
- [ ] **Accessibility score** > 95
- [ ] **Best Practices score** > 90
- [ ] **SEO score** > 90

## 🐛 Common Issues & Solutions

### Issue: Site Not Loading

**Solutions:**
1. Check GitHub Pages settings (must use GitHub Actions as source)
2. Verify workflow completed successfully in Actions tab
3. Wait 5-10 minutes for DNS propagation
4. Clear browser cache and try again

### Issue: Images Not Showing

**Solutions:**
1. Verify images are in `public/images/`
2. Check file paths use absolute paths (`/images/photo.jpg`)
3. Verify file extensions match exactly (case-sensitive)
4. Rebuild and redeploy

### Issue: Dark Mode Not Working

**Solutions:**
1. Check browser console for JavaScript errors
2. Clear localStorage: `localStorage.clear()`
3. Test in incognito/private browsing mode
4. Verify script in `BaseLayout.astro` is correct

### Issue: Build Fails

**Solutions:**
1. Check workflow logs in GitHub Actions
2. Verify all `.astro` files have valid syntax
3. Test build locally: `npm run build`
4. Check Node.js version compatibility

### Issue: Styles Not Applied

**Solutions:**
1. Verify `global.css` is in `public/styles/`
2. Check link in `BaseLayout.astro` head section
3. Hard refresh browser (Ctrl+Shift+R)
4. Clear browser cache

## 🔄 Updating Your Site

### Quick Updates (Content Only)

```bash
# Make changes to content
# ...

# Commit and push
git add .
git commit -m "Update research projects"
git push origin main
```

Deployment happens automatically!

### Major Updates (Structure/Style)

1. Create a new branch:
   ```bash
   git checkout -b redesign
   ```

2. Make changes and test locally

3. Create Pull Request on GitHub

4. Review changes

5. Merge to main (triggers automatic deployment)

## 📊 Analytics Setup (Optional)

### Google Analytics

1. Create a Google Analytics account
2. Get your GA4 Measurement ID
3. Add to `src/layouts/BaseLayout.astro` in `<head>`:

```astro
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script is:inline>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

4. Deploy changes

### Cloudflare Analytics (Privacy-Friendly)

Alternative to Google Analytics that respects user privacy.

## 🔒 Security Considerations

- [ ] No API keys or secrets in code
- [ ] No personal sensitive information exposed
- [ ] Email address protected from scrapers (consider using contact form)
- [ ] External links use `rel="noopener noreferrer"`
- [ ] HTTPS enabled (automatic with GitHub Pages)

## 🎓 Professional Tips

### Before Announcing Your Site

- [ ] Proofread all content (consider using Grammarly)
- [ ] Have a colleague review the site
- [ ] Test on different devices and browsers
- [ ] Verify all links work
- [ ] Check loading speed
- [ ] Update your email signature with site URL
- [ ] Add site to LinkedIn, Twitter, etc.

### First Week After Launch

- [ ] Monitor GitHub Actions for any issues
- [ ] Check analytics (if installed) for visitor behavior
- [ ] Test site from different networks/locations
- [ ] Gather feedback from colleagues
- [ ] Fix any reported issues quickly
- [ ] Consider announcing on social media

### Ongoing Maintenance

**Weekly:**
- Check for broken links
- Monitor site uptime

**Monthly:**
- Add new publications/talks
- Update news section
- Review and update content freshness

**Quarterly:**
- Update research project status
- Refresh teaching information
- Update metrics and impact numbers
- Review and improve SEO

**Annually:**
- Major content review
- Update profile photo if needed
- Redesign consideration
- Technology stack updates

## 📞 Support Resources

- **GitHub Pages Docs:** https://docs.github.com/en/pages
- **Astro Docs:** https://docs.astro.build
- **GitHub Actions Docs:** https://docs.github.com/en/actions

## ✅ Deployment Complete!

Once you've verified everything works:

1. **Announce your site:**
   - Update email signature
   - Add to social media profiles
   - Include in conference presentations
   - Add to business cards

2. **Share with colleagues:**
   - Get feedback
   - Exchange links with peers

3. **Submit to academic directories:**
   - Google Scholar
   - ResearchGate
   - Academia.edu
   - ORCID

4. **Monitor and maintain:**
   - Set reminder to update monthly
   - Track visits (if using analytics)
   - Keep content current

---

**Congratulations on launching your personal website!** 🎉

Your academic presence online is now established. Remember to keep it updated and let it reflect your ongoing work and achievements.

**विद्यया अमृतमश्नुते** - Through knowledge one attains immortality


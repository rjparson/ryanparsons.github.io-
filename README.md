# Ryan J. Parsons - Academic Website

A clean, professional academic website ready for GitHub Pages.

## Quick Start: Deploy to GitHub Pages

1. **Create a GitHub repository**
   - Go to github.com and create a new repository named `ryanparsons.github.io` (or any name)
   - Keep it public

2. **Upload these files**
   ```
   git init
   git add .
   git commit -m "Initial website"
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**
   - Go to repository Settings → Pages
   - Under "Source", select "Deploy from a branch"
   - Choose "main" branch, "/ (root)" folder
   - Click Save

4. **Your site will be live at:**
   - `https://YOUR_USERNAME.github.io/YOUR_REPO/`
   - (Or `https://YOUR_USERNAME.github.io/` if you named the repo `YOUR_USERNAME.github.io`)

## How to Update

### Add a new publication
Edit `index.html` and add to the publication list:
```html
<li>
    <span class="pub-year">2026</span>
    Your Name. "Paper Title." <em>Journal Name</em>.
    <a href="https://doi.org/..." class="doi">[DOI]</a>
</li>
```

### Add a working paper or replication package
1. Put the file in the `papers/` folder
2. Add a link in `index.html`:
```html
<a href="papers/your-paper.pdf">[PDF]</a>
<a href="papers/replication-package.zip">[Replication]</a>
```

### Update your CV
Replace `assets/Parsons_CV.pdf` with your updated CV.

### Update your headshot
Replace `assets/headshot.jpg` with your new photo.

## File Structure

```
├── index.html          # Main page
├── style.css           # Styling
├── assets/
│   ├── headshot.jpg    # Your photo
│   └── Parsons_CV.pdf  # Your CV
├── papers/             # Working papers & replication packages
│   └── (add PDFs and ZIPs here)
└── README.md           # This file
```

## Customization

### Colors
Edit the CSS variables at the top of `style.css`:
```css
:root {
    --navy: #14213d;        /* Main dark color */
    --accent: #457b9d;      /* Links and accents */
    --accent-light: #a8dadc; /* Light accent */
}
```

### Add Google Scholar / ORCID links
Update the footer in `index.html` with your actual profile URLs.

## To Do
- [ ] Add Google Scholar link (footer)
- [ ] Add ORCID link (footer)
- [ ] Add any additional papers to `papers/` folder

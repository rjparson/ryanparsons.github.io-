# How to Edit Your Website

This guide covers the easiest ways to update ryanjparsons.com.

---

## Quick Reference

| Task | Easiest Method |
|------|----------------|
| Edit text | GitHub website |
| Add a paper/syllabus | Local folder + Terminal command |
| Update CV | Replace file + Terminal command |

---

## Option A: Edit on GitHub (Easiest for Text Changes)

Best for: fixing typos, updating descriptions, adding a publication entry.

1. Go to https://github.com/rjparson/ryanparsons.github.io-
2. Click on `index.html`
3. Click the **pencil icon** (top right) to edit
4. Make your changes
5. Click **"Commit changes"** (green button)
6. Site updates in ~1-2 minutes

### Tips for Editing index.html

The file is organized in sections. Search (Ctrl+F or Cmd+F) for these landmarks:

- `<section id="about">` — Your bio
- `<section id="research">` — Research description and current projects
- `<section id="publications">` — Publications list
- `<section id="teaching">` — Course list
- `<section id="cv">` — CV download link

---

## Option B: Edit Locally + Push (Best for Adding Files)

Best for: adding PDFs (papers, syllabi, CV updates).

### Setup (one-time)
Your website files are at: `~/Desktop/parsons-website/`

### The Push Command
After making any local changes, run this in Terminal:

```bash
cd ~/Desktop/parsons-website && git add . && git commit -m "Update" && git push
```

You can change "Update" to something more descriptive like "Add new paper" or "Update CV".

---

## Common Tasks

### Update Your CV

1. Save your new CV as `Parsons_CV.pdf`
2. Replace the file at: `~/Desktop/parsons-website/assets/Parsons_CV.pdf`
3. Run the push command:
   ```bash
   cd ~/Desktop/parsons-website && git add . && git commit -m "Update CV" && git push
   ```

**Note:** Browsers cache PDFs. If the old version still shows, do a hard refresh (Cmd+Shift+R) or open in incognito.

---

### Add a New Publication

1. Go to https://github.com/rjparson/ryanparsons.github.io-
2. Click `index.html` → pencil icon to edit
3. Find the publications section (search for `<h3>Peer-Reviewed Articles</h3>`)
4. Copy an existing entry and modify it:

```html
<li>
    <span class="pub-year">2026</span>
    Parsons, Ryan J. "Your Paper Title." <em>Journal Name</em> Volume(Issue): Pages.
    <a href="https://doi.org/YOUR_DOI" class="doi">[DOI]</a>
</li>
```

5. Paste it in the right chronological position (newest first)
6. Commit changes

#### If you won an award:
Add this line after the DOI link:
```html
<span class="award">Winner, Award Name</span>
```

---

### Add a Working Paper (with PDF link)

1. Put the PDF in: `~/Desktop/parsons-website/papers/`
   - Name it without spaces, e.g., `ReturnMigration.pdf`

2. Push the file:
   ```bash
   cd ~/Desktop/parsons-website && git add . && git commit -m "Add working paper" && git push
   ```

3. Edit `index.html` on GitHub to add the link. Find the working papers section and change:
   ```html
   <li>"Your Paper Title"</li>
   ```
   To:
   ```html
   <li><a href="papers/ReturnMigration.pdf">"Your Paper Title"</a></li>
   ```

---

### Add a New Syllabus

1. Put the PDF in: `~/Desktop/parsons-website/syllabi/`
   - Name it without spaces, e.g., `SOC499.pdf`

2. Push the file:
   ```bash
   cd ~/Desktop/parsons-website && git add . && git commit -m "Add syllabus" && git push
   ```

3. Edit `index.html` on GitHub. Find the teaching section and add:
   ```html
   <li><a href="syllabi/SOC499.pdf">SOC 499: Course Name</a></li>
   ```

---

### Add a New Course (No Syllabus)

Edit `index.html` on GitHub and add to the teaching list:
```html
<li>SOC 499: Course Name</li>
```

---

### Update Your Bio

1. Edit `index.html` on GitHub
2. Find `<section id="about">`
3. Edit the text between `<p>` and `</p>` tags
4. Commit changes

---

### Update Research Projects

1. Edit `index.html` on GitHub
2. Find `<section id="research">`
3. Each project is in this format:
   ```html
   <li><strong>Project Name:</strong> Description here.</li>
   ```
4. Add, edit, or remove projects as needed
5. Commit changes

---

## File Structure

```
~/Desktop/parsons-website/
├── index.html          ← Main page (edit text here)
├── style.css           ← Styling (colors, fonts)
├── assets/
│   ├── headshot.jpg    ← Your photo
│   └── Parsons_CV.pdf  ← Your CV
├── papers/             ← Working papers & replication packages
└── syllabi/            ← Course syllabi
```

---

## Troubleshooting

### Changes not showing up?
- Wait 1-2 minutes for GitHub Pages to deploy
- Hard refresh: Cmd+Shift+R (Mac) or Ctrl+Shift+R (Windows)
- Try incognito/private window

### PDF showing old version?
- Add `?v=2` to the URL: `ryanjparsons.com/assets/Parsons_CV.pdf?v=2`
- Or clear browser cache

### Push command fails?
Make sure you're in the right folder:
```bash
cd ~/Desktop/parsons-website
```

Then try again:
```bash
git add . && git commit -m "Update" && git push
```

### "Nothing to commit" message?
This means no files have changed since your last push. If you updated a file, make sure you saved it.

---

## Getting Help

You can always ask Claude to make edits for you. Just describe what you want to change, and Claude can edit the files and push them to GitHub.

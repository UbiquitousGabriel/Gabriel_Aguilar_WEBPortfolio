# Customization Guide

Everything you need to make this portfolio your own. All edits happen inside `index.html` — search for the section headers below to find the right spot quickly. In most text editors you can use **Cmd+F** (Mac) or **Ctrl+F** (Windows) to search.

---

## 1. Your Photo

**Find:** `<div class="home-photo-box"><span>PHOTO</span></div>`

**Replace with:**
```html
<img src="assets/images/your-photo.jpg"
     alt="Gabriel Aguilar"
     style="width:175px;height:235px;object-fit:cover;display:block;" />
```

Then create an `assets/images/` folder and drop your photo in there.

---

## 2. Bio Text

**Find:** `<!-- TO CUSTOMIZE: Edit this paragraph with your bio text -->`

Replace the paragraph text between the `<p class="home-bio-text">` tags with your actual bio.

---

## 3. Contact Info

**Find:** `<!-- TO CUSTOMIZE: Update phone and email below -->`

Update the two `<a>` tags:
```html
<a class="home-contact-link" href="tel:YOUR10DIGITNUMBER">(XXX) XXX-XXXX</a>
<a class="home-contact-link" href="mailto:YOUR@EMAIL.COM">your@email.com</a>
```

---

## 4. Résumé PDFs

**Step 1:** Drop your PDF files into the `assets/pdfs/` folder.

Name them clearly, for example:
```
assets/pdfs/gabriel-aguilar-film.pdf
assets/pdfs/gabriel-aguilar-theater.pdf
assets/pdfs/gabriel-aguilar-creative-tech.pdf
```

**Step 2:** Find `ALL_CLUSTERS` in the JavaScript section of `index.html`.

For each cluster, update the `resumeFile` value:
```javascript
resumeFile: "/assets/pdfs/gabriel-aguilar-film.pdf",
```

**Step 3:** Find the center label click handler and replace the `alert()`:
```javascript
// Find this line:
alert('Open résumé: ...');

// Replace with:
window.open(clusterData.resumeFile, '_blank');
```

---

## 5. Skill Words and Bullet Points

**Find:** `const ALL_CLUSTERS = [` in the JavaScript section.

Each cluster looks like this:
```javascript
{
  label: "FILM",              // The big center word
  labelFontSize: 28,          // Font size of center word (reduce if label is long)
  resumeFile: "/assets/pdfs/gabriel-aguilar-film.pdf",
  words: [
    {
      t: "Video Editing",     // The skill word shown in the cluster
      summary: "Post-production editing for narrative and commercial projects.",  // One-line description shown on hover
      bullets: [              // Bullet points shown in the detail panel
        "Your real experience here",
        "Another project or achievement",
        "A tool, technique, or context",
      ]
    },
    // ... more words
  ]
}
```

**To add a skill word:** Copy an existing `{ t: ..., summary: ..., bullets: [...] }` block and paste it into the `words` array.

**To remove a skill word:** Delete the entire `{ ... }` block for that word.

**To update bullet points:** Replace the `getLoremBullets(4)` placeholder with a real array of strings:
```javascript
bullets: [
  "Edited 3 short films for festival submission, 2022–2023.",
  "Managed multi-camera live event cuts for 500+ person audiences.",
  "Proficient in Premiere Pro, DaVinci Resolve, and Final Cut Pro.",
]
```

---

## 6. Portfolio Projects

**Find:** `const ALL_PROJECTS = [` in the JavaScript section.

Each project looks like this:
```javascript
{
  title: "Short Film: Meridian",
  category: "Film",           // Shown as a small label above the title
  description: "Your project description goes here.",
  imageCount: 4               // Number of image slots shown in the lightbox
}
```

**To add a project:** Copy an existing block and paste it into the array.

**To add real project images:** Inside `openLightbox()`, replace the placeholder SVG with real `<img>` tags. The relevant section is marked with:
```
/* TO CUSTOMIZE: Replace makePlaceholderImageSVG() with real <img> tags */
```

---

## 7. Discipline Tags (Home Page)

**Find:** `<!-- TO CUSTOMIZE: Add or remove discipline tags here -->`

Add or remove `<span>` elements:
```html
<div class="home-discipline-tags">
  <span>Film</span>
  <span>Theater</span>
  <span>Creative Technology</span>
</div>
```

---

## 8. Page Title (Browser Tab)

**Find:** `<title>Gabriel Aguilar</title>` near the top of the file.

Change it to whatever you want shown in the browser tab.

---

## 9. Colors

The site is intentionally black and white. If you ever want to introduce a single accent color, search for `rgba(0,0,0` in the CSS and adjust specific values. The main background is set on `html, body` near the top of the `<style>` block.

---

## Deploying to GitHub Pages

1. Push this folder to a GitHub repository
2. Go to your repository → **Settings** → **Pages**
3. Under "Build and deployment", set Source to **Deploy from a branch**
4. Set branch to `main`, folder to `/ (root)`
5. Click **Save**
6. Your site will be live in ~60 seconds at `https://yourusername.github.io/repo-name/`

---

*Any questions or bugs — open an issue on the repository.*

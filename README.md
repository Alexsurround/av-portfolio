# Alexandr Fedorov — AV Portfolio

Personal portfolio website for AV Systems Engineer projects.

**Live site:** https://YOUR-USERNAME.github.io/av-portfolio/

---

## How to add or edit a project

Open `projects.json` and edit the array. Each project looks like this:

```json
{
  "id": 7,
  "title": "New Concert Hall",
  "location": "Praha, Czech Republic",
  "year": "2024",
  "category": "Concert Hall",
  "description": "Project description here.",
  "equipment": [
    "L-Acoustics K2 (12)",
    "L-Acoustics LA12X (3)"
  ],
  "photos": [
    "./media/new-hall/main.jpg",
    "./media/new-hall/stage.jpg"
  ],
  "pressLinks": [
    { "label": "Article title", "url": "https://..." }
  ],
  "videoUrl": "https://youtube.com/watch?v=...",
  "featured": true
}
```

**Categories:** `Concert Hall` · `Theatre & Opera` · `Cinema & Dolby` · `Casino & Club` · `Hotel & Hospitality` · `Corporate & Q-SYS`

---

## How to add photos

1. Create a folder: `media/project-name/`
2. Put photos there: `main.jpg`, `gallery-1.jpg`, etc.
3. Reference in `projects.json`: `"./media/project-name/main.jpg"`
4. Commit and push — site updates automatically

---

## Structure

```
av-portfolio/
├── index.html          ← the site (do not edit unless changing design)
├── projects.json       ← ALL project data — edit this to update content
├── README.md
└── media/
    ├── odessa-opera/
    ├── cinema-city/
    ├── emily-resort/
    │   ├── main.jpg
    │   └── gallery-1.jpg
    └── ...
```

---

## Deploy to GitHub Pages

1. Push this folder to a GitHub repository
2. Go to **Settings → Pages**
3. Source: **Deploy from a branch** → `main` → `/ (root)`
4. Save — site is live in ~1 minute

---

## Local preview

```bash
# Python
python3 -m http.server 8080

# Then open: http://localhost:8080
```

> Note: opening `index.html` directly (file://) won't work because of the `fetch('./projects.json')` call. Always use a local server or deploy to GitHub Pages.

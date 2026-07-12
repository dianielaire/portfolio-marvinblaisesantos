# Marvin Blaise C. Santos — Portfolio

A single-page portfolio site. Projects are stored in `projects.json` and
images in `/images`, both committed to this repo — no backend needed.

## Files

```
index.html       the whole site (HTML/CSS/JS)
projects.json     your project list (starts empty: [])
images/           project screenshots go here
```

## 1. Put this on GitHub

```bash
cd portfolio          # this folder
git init
git add .
git commit -m "initial site"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

## 2. Turn on GitHub Pages

1. On GitHub, open your repo → **Settings** → **Pages**.
2. Under "Build and deployment", set **Source** to `Deploy from a branch`.
3. Branch: `main`, folder: `/ (root)`. Save.
4. After a minute, your site is live at:
   `https://<your-username>.github.io/<repo-name>/`

## 3. Add a project

1. Open `index.html` in a browser (works locally too, once served —
   see note below) and click **+ Add Project**.
2. Fill in the title, description, tags, and choose your screenshots.
3. Click **Generate Entry**. It shows you:
   - which filenames to save your screenshots as, in `/images`
   - a JSON block to copy
4. Save your screenshots into `images/` using the exact filenames shown.
5. Open `projects.json` and paste the JSON block inside the `[ ]` array
   (add a comma between entries if there's more than one).
6. Commit and push:
   ```bash
   git add .
   git commit -m "add project: <title>"
   git push
   ```
7. Refresh your GitHub Pages URL — the new card is live for everyone.

**Note:** Browsers block a page from loading local JSON files when opened
directly (`file://...`). To preview `projects.json` locally before pushing,
run a quick local server from the project folder:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000` in your browser.

## Example `projects.json` entry

```json
[
  {
    "id": 1,
    "title": "Inventory Dashboard",
    "desc": "Internal tool for tracking stock levels across stores.",
    "tags": ["C#", ".NET", "SQL Server"],
    "images": ["images/inventory-dashboard-1.png"]
  }
]
```

# Jhon Chris Alipao — Portfolio

Personal portfolio site — GIS &amp; Remote Sensing work, experience, and a field-notes gallery of maps and outputs.

## Publish it on GitHub Pages

1. Create a new **public** repository on GitHub (e.g. `portfolio`, or name it `<your-username>.github.io` if you want it at the root of your GitHub domain).
2. Add these files to the repo — either drag-and-drop through the GitHub web UI, or via git:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source: Deploy from a branch**, **Branch: main**, folder **/ (root)**. Save.
5. Wait a minute or two, then your site is live at:
   - `https://<your-username>.github.io/` (if the repo is named `<your-username>.github.io`), or
   - `https://<your-username>.github.io/<repo-name>/` otherwise.

## Updating the text (bio, experience, projects, skills, certifications)

All of that content lives directly in `index.html`. Open the file, find the section (they're marked with HTML comments like `<section id="projects">`), and edit the text. Commit and push — the live site updates automatically.

## Adding a map to the Field Notes gallery

This site is static (no database), so maps are added by editing a file, not by uploading through the browser:

1. Drop your image into `images/maps/`.
2. Open `index.html`, scroll to the `<script>` near the bottom, and find the `fieldNotes` array. Add an entry:
   ```js
   {
     title: "Deforestation hotspot map — CADT 4",
     category: "Deforestation & Forest Monitoring", // or "InSAR & Hazard", "CLUP / CDRA", "Drone / UAV", "Research"
     caption: "CUSUM-based change detection output, Q2 2026.",
     dateLabel: "July 2026",
     image: "images/maps/cadt4-hotspot.jpg"
   }
   ```
3. Commit and push.

## Folder structure

```
index.html
images/
  profile.jpg
  maps/        ← put new map images here
```

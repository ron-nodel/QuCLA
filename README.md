# Quantum Device Modeling Group, UCLA

Static website for the Gyure / Anderson group at the UCLA Center for Quantum Science and Engineering.
Plain HTML and CSS, no build step, no dependencies. Works on Vercel, Netlify, GitHub Pages, or any static host.

## Files

```
index.html          home: intro, group, projects (tabbed), open projects, publications, contact
collaborators.html  collaborators page
style.css           all styling (UCLA palette, responsive breakpoints at 900 px and 720 px)
images/
  cqse-logo.png
  group-photo.jpg
  people/face1.jpg ... face8.jpg   stand-in headshots cropped from the group photo
```

## Editing

**Headshots.** Each person in the Group section has
`<div class="headshot" data-person="…"><img src="images/people/…"></div>`.
Replace the image path. Square images look best (they are displayed 1:1, `object-fit: cover`).
The same file is used for the small face next to the person's name on project rows (`<img class="face" …>`).

**Project pictures.** Each project row has `<div class="pic"><div class="placeholder">[…]</div></div>`.
Replace the placeholder div with `<img src="images/….png" alt="…">`. A 16:10 image fits without cropping.

**Projects and tabs.** Projects live inside `<div class="panel" id="theme-…">` blocks, one per tab.
The tab buttons are in `<div class="tabs">`; `data-theme` on a button must match the panel id after `theme-`.
A link with the tab name as hash (`index.html#valley`) opens that tab on load.

**Publications.** Two places: the "Selected publications" list under each project, and the full list in `#publications`.

**Deploy.** Push to GitHub, then import the repo in Vercel (framework preset: Other, no build command, output directory `.`).
For GitHub Pages, enable Pages on the `main` branch, root folder.

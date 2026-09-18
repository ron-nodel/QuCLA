# Quantum Device Modeling Group website

Plain HTML, no build step. Hosted with GitHub Pages.

## Files

- `index.html` – the whole site: intro, group, projects, open projects, publications, talks, contact
- `collaborators.html` – collaborators page
- `style.css` – styling
- `images/` – pictures. See `images/README.md` for what to upload and what to call it.

## Editing

Open `index.html` and edit the text directly.

- Projects sit in `<div class="panel" id="theme-...">` blocks, one per tab. To add a project, copy an existing `<article class="project">` and change the text.
- Publications are in `#pubs-list`, talks in `#talks-list`. Newest first. Rows after the first 10 papers / 6 talks have `class="more" hidden` so they sit behind the Show all button.
- A link like `index.html#valley` opens that tab directly.
- Clicking a person (blue names, in the Group section or next to a project) slides in a panel with their projects, publications and talks. It is built by the script at the bottom of `index.html` from the same lists, so it stays in sync on its own. To add a Google Scholar or personal link for someone, find their entry in the `PERSONS` object in that script and fill in `"scholar"`.

## Deploy

Push to `main`. GitHub Pages rebuilds in a minute or two.

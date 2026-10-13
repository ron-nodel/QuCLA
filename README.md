# Quantum Device Modeling Group website

Plain HTML, no build step. Hosted with GitHub Pages.

## Files

- `index.html` – the whole site: intro, group, projects, open projects, publications, talks, contact. Work that is under way goes in the project tabs. Open projects is only for ideas nobody has picked up yet.
- `collaborators.html` – collaborators page
- `style.css` – styling
- `images/` – headshots, project pictures and collaborator logos. See `images/README.md` for what to upload and what to call it.

## Editing

Open `index.html` and edit the text directly.

- Projects sit in `<div class="panel" id="theme-...">` blocks, one per tab. Each project is an `<article class="project">` that shows only its title until clicked. To add one, copy an existing article and change the text, then give it a new `id` and update the ids that are built from it (`<id>-btn`, `<id>-body`, and `aria-controls`), or the new row won't open.
- The search box needs no upkeep. It reads whatever is on the page when it loads, so new projects, people and papers become searchable on their own.
- Publications are in `#pubs-list`, talks in `#talks-list`. Newest first. Rows after the first 10 papers / 6 talks have `class="more" hidden` so they sit behind the Show all button.
- A link like `index.html#valley` opens that tab, and `index.html#radiation` opens that project.
- Clicking a person (blue names, in the Group section or next to a project) slides in a panel with their projects, publications and talks. That panel reads from the `PERSONS` object in the script at the bottom of `index.html`. When you add a paper or talk, add it to each group author's `pubs` there too. The `"scholar"` field takes a Google Scholar or personal link.

## Deploy

Push to `main`. GitHub Pages rebuilds in a minute or two.

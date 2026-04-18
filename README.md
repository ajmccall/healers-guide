# A Panicked Healer's Guide

A fan-made static web page that presents a lore-inspired healing reference for a Warriors-style world, with a toggle between fictional usage and real-world reference notes.

## What this project is

This repository contains a single-page static site intended for:
- browsing herbs, remedies, illnesses, poisons, techniques, and healer tasks
- searching by symptom or topic
- comparing "Ancestors' Lore" with "Twoleg Truth"
- eventually publishing via GitHub Pages

## Files

- `index.html` — the full site, including HTML, CSS, data, and JavaScript

## Improvements made

I reviewed the original page and made these improvements:
- added better page metadata for browsers and sharing
- improved semantic structure with `header`, `main`, `section`, `article`, and `footer`
- added accessibility improvements:
  - skip link
  - better labels
  - `aria` attributes for navigation and mode toggle
  - live no-results message
- improved mobile responsiveness
- added a visible fan-project disclaimer
- improved search so it also matches:
  - descriptions
  - ingredient names
  - uses
  - code entries
- made the code section filterable during search
- added a no-results state
- cleaned up a few wording issues and warnings

## Run locally

Because this is a static page, you can open it directly in your browser:

```bash
open index.html
```

Or serve it locally with a simple server:

```bash
python3 -m http.server 8080
```

Then visit:

```text
http://localhost:8080
```

## Publish with GitHub Pages

### Option 1: Deploy from the root of the repository

If this repository is only for this site:
1. Push the repo to GitHub.
2. Go to **Settings** → **Pages**.
3. Under **Build and deployment**, choose:
   - **Source:** Deploy from a branch
   - **Branch:** `main` (or `master`)
   - **Folder:** `/ (root)`
4. Save.
5. GitHub will publish `index.html` automatically.

### Option 2: Deploy from `/docs`

If this is part of a larger repo, move the site into a `docs/` folder and publish from there.

## Recommended next improvements

### Content improvements
- add more herbs and illnesses from the source material
- add source notes for each entry
- add a glossary for terms like `greencough`, `whitecough`, `queen`, and `Twoleg`
- separate lore facts from real-world plant notes more clearly
- include a clear copyright/fan disclaimer section

### Technical improvements
- split the large `index.html` into:
  - `index.html`
  - `styles.css`
  - `script.js`
  - `data/*.json`
- add Open Graph metadata for nicer link previews
- add a `404.html` page for GitHub Pages
- add a favicon and social preview image
- add a light performance pass by removing unused Tailwind dependency if you keep mostly custom CSS
- replace inline `onclick` handlers with JavaScript event listeners

### UX improvements
- add filter chips by category
- add a sticky search summary, such as “12 results found”
- add a “back to top” button
- let users expand/collapse categories
- highlight matching search terms in results
- add bookmarkable search using URL parameters like `?q=bleeding`

## Important publishing note

This appears to be a fan work inspired by **Warriors**. Before publishing publicly, I suggest adding:
- an explicit statement that this is an unofficial fan project
- a non-commercial disclaimer
- proper credit to the original creators
- a note that the plant information is not real medical or foraging advice

## Suggested project roadmap

1. Publish the current static page to GitHub Pages.
2. Split code into separate files.
3. Move the herb data into JSON.
4. Add images or illustrations.
5. Add citations and disclaimers.
6. Improve SEO and social sharing.

If you want, I can next:
- split this into `index.html`, `styles.css`, and `script.js`
- add GitHub Pages-friendly polish like `404.html` and social metadata
- help you turn the herb data into a cleaner JSON data file
- make the site look more polished for public release

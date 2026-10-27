# maivansang.github.io

Personal landing page for Mai Van Sang — Project Manager.

Published with GitHub Pages at <https://maivansang.github.io>.

## Stack

Plain HTML, CSS and JavaScript — no build step, no dependencies. Open
`index.html` and it runs.

## Layout

| Path | Purpose |
| --- | --- |
| `index.html` | Page markup. Translatable nodes are tagged `data-i18n` / `data-i18n-html`. |
| `styles.css` | All styling, including the responsive breakpoints at 1040px, 860px and 640px. |
| `script.js` | Japanese/English dictionaries plus the language switcher and footer year. |
| `img/` | Hero cover and avatar. |

### Translations

`script.js` holds a `translations` object with a `ja` and an `en` dictionary.
Both must carry the same keys — a node whose key is missing from one language
renders empty when that language is selected.

### Hero cover

`img/team-cover.jpg` is 915×610 (exactly 3:2). `.hero-cover-card` pins the same
`aspect-ratio: 3 / 2` and the image uses `object-fit: contain`, so the whole
photo is shown uncropped at every width. Replacing the image with a different
aspect ratio means updating that `aspect-ratio` to match, otherwise the frame
letterboxes.

## Running locally

```bash
python3 -m http.server 4600
```

Then open <http://localhost:4600>. A plain file:// open also works, but serving
over HTTP matches how Pages behaves.

## Deploying

GitHub Pages builds from `main`. Pushing to `main` publishes; the rebuild
usually lands within a couple of minutes.


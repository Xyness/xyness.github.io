# xyness.github.io

The source of [xyness.github.io](https://xyness.github.io/), my portfolio. One HTML file with its
CSS and JavaScript inline, no build step, no framework, nothing loaded from another domain.

## Running it

Open `index.html`, or serve the folder to get exactly what GitHub Pages serves:

```bash
python3 -m http.server
```

## How it's put together

The English text lives in the markup. The French lives in a dictionary at the bottom of the
second script, keyed by the `data-i18n` attributes. There is no English dictionary to keep in
sync: it's read back from the page on load, and a French key that's missing shows up as a
warning in the console.

Theme and language are remembered in `localStorage`. `?lang=fr` and `?theme=light` take
precedence, so a link can open the page in French whatever the visitor chose before. With
nothing stored, a browser set to French gets French.

The fonts are self-hosted WOFF2 files: Space Grotesk for headings, Inter for text, JetBrains Mono
for labels. Their licences sit next to them in `fonts/`.

The terminal screenshots are crops of each project's `docs/demo.svg`, rendered at twice the size
they're displayed at and saved as lossless WebP, which comes out smaller than lossy for flat
terminal colours.

## Known limits

Search engines only see the English version, since the French one is swapped in by JavaScript.
The screenshots are made by hand, so they fall behind when a project's output changes.

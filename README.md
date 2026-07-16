# Molecule Synth website

The static website for [moleculesynth.com](https://moleculesynth.com), a physical electronics synthesizer and experimenter's design set.

## Local preview

The site has no build step or runtime dependencies. From the repository root:

```sh
python3 -m http.server 4173
```

Then open `http://localhost:4173`.

## Structure

- `index.html` — semantic single-page site and content
- `style.css` — responsive design system and layouts
- `js/site.js` — mobile navigation and progressive reveal behavior
- `images/` — original Molecule Synth photography and archival graphics
- `manual.pdf` — original user manual

The site is published from the repository root through GitHub Pages. The `CNAME` file must remain `moleculesynth.com`.

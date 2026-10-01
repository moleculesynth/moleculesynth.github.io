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

## Security maintenance

The homepage uses a meta Content Security Policy allowing local scripts, styles,
images, and the existing YouTube privacy-enhanced embed. Inline executable scripts,
other remote resources, plugins, base URL overrides, and form submissions are blocked.
Its referrer policy is `strict-origin-when-cross-origin`.

The ML1, ML2, and ML3 demos retain their existing libraries and policies; their
modernization is deferred. Their CDN dependencies need a separate review:
Dependabot does not provide coverage for these HTML script URLs.

GitHub Pages serves this site directly. HSTS, `X-Content-Type-Options`, and
anti-framing protection require HTTP response headers configured at a supported
hosting/proxy layer. Meta tags cannot implement those protections. No hosting or
DNS change is part of this cleanup.

# Rishi & Vishnupriya — Wedding Countdown (source)

## Files
- `index.html` — page structure/content only
- `styles.scss` — edit this for styling (colors, sizes, spacing, animations)
- `styles.css` — compiled output that `index.html` actually loads (regenerate after editing the .scss)
- `script.js` — countdown, petals, opening animation, slideshow, ambient music

## Preview locally
Just open `index.html` in a browser. No build step is required to *view* it —
`styles.css` is already compiled and committed.

## Editing the styles
If you change `styles.scss`, recompile it to `styles.css`:

```bash
npm install -g sass      # one-time install
sass styles.scss styles.css
```

(or use any Sass/VS Code extension that watches and compiles on save)

## Adding your photos, music & map (assets/ folder)
Drop your real files straight into these folders — the site picks them up
automatically, no code changes needed:

```
assets/
  photos/
    photo-1.jpg   \
    photo-2.jpg    \__ shown in the "Our story so far" slideshow, in order
    photo-3.jpg    /
    photo-4.jpg   /
  music/
    background.mp3   — plays once the seal is tapped open
  directions/
    venue-map.jpg     — optional preview image above "Get Directions"
```

Each one has a fallback if the file isn't there yet: missing photos show the
placeholder icon, missing music falls back to a soft generated chime, and a
missing map image just doesn't show — nothing breaks either way. See the
`.txt` file inside each folder for exact filename/format notes.

## Things you'll likely want to change first
- **Names & date**: search `index.html` for "Emma", "James", "20th March 2027"
- **Countdown target**: `const weddingDate = new Date('2027-03-20T16:00:00');` in `script.js`
- **Venue/address**: search `index.html` for "The Ivy Garden Estate"
- **Photos, music, map**: see the `assets/` section above
- **Colors**: the `:root { --gold: ...; --wine: ...; }` block at the top of `styles.scss`

## Hosting this yourself
This split version is for editing. To put it online, either:
1. Upload all four files (`index.html`, `styles.css`, `script.js`) to any static
   host (Netlify, Vercel, GitHub Pages, etc.), or
2. Ask Claude to merge it back into one self-contained HTML file and publish
   it as a claude.ai artifact link — that's the version currently live and
   shareable with your guests.

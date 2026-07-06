# PMAB — Pro-Metabolic Animal-Based

**A lightweight, static grocery reference tool** built on Ray Peat bioenergetic principles and Paul Saladino animal-based framework.

---

## Files

```
pmab/
├── index.html     ← everything (HTML, CSS, JS)
├── data.js        ← all food data (JSON-style JS object)
└── README.md      ← this file
```

## Running locally

Just open `index.html` in a browser. No build step, no server, no dependencies to install. Lucide icons and Google Fonts load from CDN.

## Deploying (free)

**Netlify (recommended):**
1. Drag the `pmab/` folder to netlify.com/drop
2. Done. Get a URL instantly.
3. Connect a domain like pmab.io later.

**Vercel:**
```bash
npm i -g vercel
cd pmab
vercel
```

**GitHub Pages:**
Push to a repo → Settings → Pages → Deploy from main branch.

---

## Extending

### Add a food item
In `data.js`, find the right category and add to `items[]`:
```js
{ name: "Food name", note: "Why it's included", starred: true }
```
`starred: true` shows the "★ staple" badge.

### Add a category
Add a new object to `PMAB_DATA.categories[]`:
```js
{
  id: "unique-id",
  label: "Display Name",
  emoji: "🫐",
  color: "#hex",
  note: "Category philosophy note",
  items: [ ... ]
}
```

### Change the color scheme
Edit CSS variables in `:root` inside `index.html`.

---

## Next pages to build

- `/principles.html` — Peat vs Saladino synthesis explainer
- `/meals.html` — meal templates using only approved foods
- `/avoid.html` — expanded avoid list with the "why" 
- `/swaps.html` — anti-PUFA ingredient swapper tool

---

## Tech used

- Vanilla HTML/CSS/JS — zero frameworks
- [Lucide Icons](https://lucide.dev) via unpkg CDN
- [Google Fonts](https://fonts.google.com) — Zilla Slab + Inter
- All data lives in `data.js` — easy to edit, no database needed

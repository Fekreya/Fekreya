# Website folder . map

Everything that renders on `fekreya.com` lives here. Static HTML. No build step.

---

## Folder layout

```
/website/
├── README.md                     ← this file
│
├── index.html                    ← Homepage. The landing page.
├── showcase.html                 ← Hero animation. Embedded as an iframe inside index.html.
├── join.html                     ← Hiring page for senior executive assistants.
│
├── hero-loop.html                ← Alternate hero loop concept (not embedded).
├── website-hero-animation.html   ← Earlier hero animation prototype.
├── inbox-zero.html               ← Standalone inbox-to-zero visual (concept sketch).
│
└── _archive/                     ← Prior versions kept for reference. Do not touch.
```

---

## Live pages vs. concept sketches

| File | Live on fekreya.com? | Notes |
|---|---|---|
| `index.html` | **Yes** | Homepage. Edit here for copy or layout changes. |
| `showcase.html` | **Yes** (iframe in index) | The looping hero animation. Ten scenes. Scene 1 is the brand intro; scenes 2-10 tell the founder's day. |
| `join.html` | **Yes** | Standalone hiring page. |
| `hero-loop.html` | No | Alternate hero concept. Kept for reference. |
| `website-hero-animation.html` | No | Earlier animation prototype. Kept for reference. |
| `inbox-zero.html` | No | Standalone concept sketch. |

---

## Editing the hero animation

The animation lives entirely in `showcase.html`.

Each scene is a `<section class="scene" data-duration="XXXX">`. `data-duration` sets how long the scene stays on screen in milliseconds. Animations inside each scene use CSS keyframes gated on `#scene-N.active` selectors.

The scene order is: brand intro → morning brief → WhatsApp + board → email to task → decision → calendar → travel → inbox to zero → sleep → strategy brief. Then loops back to brand intro.

---

## Brand rules . never break

- **No em dashes** in copy. Periods and hyphens only.
- **No city names** anywhere visible.
- **Only `team@fekreya.com`** for email contact.
- **Phone number invisible** in copy. Only in the WhatsApp link href (`wa.me/201131561330`).
- **Cream `#fdfaf2`** default background. **Navy `#0F1830`** text. **Coral `#E87A5D`** italic accents.
- **Plus Jakarta Sans** body. **Space Grotesk** display.
- **Executive assistant** or **EA**. Never bare "assistant."

---

## Deploying

Static hosting. Push to GitHub, deploy from `website/`.

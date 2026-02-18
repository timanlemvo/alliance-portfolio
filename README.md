# alliance-portfolio

Source for [tima.dev](https://tima.dev). Single-file portfolio site for Tima Nlemvo, Senior IT Engineer.

---

## What This Is

A self-contained `Index.html` that serves as a full interactive portfolio. No build step, no dependencies, no framework. Pure HTML, CSS, and vanilla JS.

> **Note:** This single-file approach is temporary. The site will be migrated to [Astro](https://astro.build) as I learn the framework.

**Live site:** [tima.dev](https://tima.dev)

---

## Structure

```
alliance-portfolio/
├── Index.html       # The entire site
└── NewMemoji.png    # Avatar asset
```

Everything lives in `Index.html`:

- Inline CSS with CSS custom properties for dark/light theming
- Vanilla JS for view routing (SPA-style navigation without a router)
- Ghost Content API fetch for live blog posts from [holocron-labs.tima.dev](https://holocron-labs.tima.dev)
- No build pipeline, no npm, no bundler

---

## Sections

| Section | Description |
|---------|-------------|
| Home / Bridge | Hero, Professional Alignment Matrix, quick-nav cards |
| The Fleet | 3-node Proxmox cluster specs, network topology, services |
| Projects | SIEM pipeline, zero-trust identity platform, GPU AI platform |
| Holocron Logs | Live Ghost CMS posts + featured incident writeup |
| About | Background, work history, principles |
| Contact | Email copy, LinkedIn, GitHub |

---

## Ghost CMS Integration

Latest posts are fetched live from the Ghost Content API on first visit to the Holocron section.

```js
const GHOST_API_URL = 'https://holocron-labs.ghost.io';
const GHOST_URL    = 'https://holocron-labs.tima.dev';
```

Pulls `title`, `slug`, `custom_excerpt`, `published_at`, `feature_image`, and `tags` for the 6 most recent posts. Cards display `custom_excerpt` as the subtitle. Set this field in Ghost admin on each post for clean card copy.

---

## Deployment

Static file. Deploy anywhere that serves HTML.

**Current setup:** [tima.dev](https://tima.dev)

To run locally:
```bash
npx serve .
# or
python3 -m http.server 8080
```

---

## Related Repos

| Repo | Description |
|------|-------------|
| [Alliance-homelab-infrastructure](https://github.com/timanlemvo/Alliance-homelab-infrastructure) | Homelab configs, documentation, and architecture |
| [technical-writeups](https://github.com/timanlemvo/technical-writeups) | In-depth engineering writeups sourced by the Holocron blog |

---

[tima.dev](https://tima.dev) · [holocron-labs.tima.dev](https://holocron-labs.tima.dev) · [linkedin.com/in/timanlemvo](https://linkedin.com/in/timanlemvo)

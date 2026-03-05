# anujan — portfolio

Minimal, static portfolio built with [Astro](https://astro.build). Zero client-side JavaScript. Hosted on Netlify.

## Quick Start

```bash
npm install
npm run dev       # local dev server at localhost:4321
npm run build     # production build to dist/
npm run preview   # preview production build locally
```

## Editing Content

All site content lives in **`src/data/site.json`**. Edit it directly on GitHub — no code changes needed.

You can modify:
- Name, about text, and incoming roles
- Work experience entries
- Entrepreneurial highlights
- Social links and URLs

### Sections format

Each section item supports these fields:

| Field       | Required | Description                        |
| ----------- | -------- | ---------------------------------- |
| `text`      | yes      | Main text before company/link      |
| `company`   | no       | Bolded company name                |
| `suffix`    | no       | Text after the company name        |
| `linkText`  | no       | Linked text (e.g. "Toona.io")     |
| `linkUrl`   | no       | URL for the linked text            |

## Resume

Drop your resume PDF at **`public/resume.pdf`**. It will be:
- Embedded at `/resume`
- Downloadable via the download button

To swap it out, just replace the file.

## Deploying to Netlify

1. Push to GitHub
2. Connect the repo in Netlify
3. Build settings are already configured in `netlify.toml`

That's it — Netlify will auto-deploy on every push.

## Project Structure

```
src/
├── components/
│   └── Icon.astro          # SVG icon component (4 icons)
├── data/
│   └── site.json           # ← all editable content
├── layouts/
│   └── Base.astro          # HTML shell, meta, fonts
├── pages/
│   ├── index.astro         # Home page
│   └── resume.astro        # Resume viewer
└── styles/
    └── global.css          # All styles (~150 lines)
public/
└── resume.pdf              # Your resume (replace this)
```

## Performance

- **Zero JS** shipped to the browser
- **~2KB CSS** (one file, inlined by Astro)
- **Static HTML** output — no server, no hydration
- **Preconnected** Google Fonts with `font-display: swap`

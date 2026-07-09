# LumaDeck Website

Marketing + docs site for **LumaDeck: Immersive Light Sync** — live at [www.luma-deck.com](https://www.luma-deck.com).

Plain static HTML/CSS/JS — no build step, no dependencies. Deployed on Netlify.

## Structure

```
public/                     ← Netlify publish directory
  index.html                Landing page (horizontal slide deck on desktop, vertical scroll on mobile)
  manual.html               User manual (sticky TOC + scroll-spy)
  demo.html                 Product demo (YouTube embed placeholder)
  robots.txt, sitemap.xml
  assets/
    css/theme.css           Bundled design-system tokens (colors, type, spacing, effects, base)
    css/site.css            Shared component styles (header, badges, buttons, glow, animations)
    img/                    Optimized images
netlify.toml                publish = "public", no build command
docs/                       Design handoff + source material (NOT deployed)
```

Built from the Claude Design handoff in `docs/lumadeck-website-prototype/`. The prototypes there use a
proprietary design-tool runtime; the pages in `public/` are the production rebuild (visually matched,
dependency-free).

## Local preview

```
cd public && python3 -m http.server 8123
# open http://localhost:8123
```

## To finish the demo page

Open `public/demo.html`, find `var VIDEO_ID = "";` near the bottom, and paste the YouTube video ID.
The placeholder swaps to a real embed automatically.

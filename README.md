# Ironwood Plumbing, Heating & Cooling

A marketing website for **Ironwood Plumbing, Heating & Cooling** — a fictional, family-owned
home services company in the fictional town of Maple Grove. This is a demo/portfolio project
only; Ironwood is not a real business.

Built with [Astro](https://astro.build) and [Tailwind CSS v4](https://tailwindcss.com).

## 🚀 Project Structure

```text
/
├── public/
│   └── favicon.svg
├── src/
│   ├── assets/
│   │   └── images/          # Source photos, optimized at build time via astro:assets
│   ├── components/
│   │   ├── Header.astro      # Sticky nav, Google-reviews strip, mobile menu
│   │   └── Footer.astro
│   ├── layouts/
│   │   └── Layout.astro      # Shared <head>, demo banner, header/footer wrapper
│   ├── pages/
│   │   ├── index.astro       # Home
│   │   ├── services.astro    # Services + FAQ accordion
│   │   ├── about.astro       # Company story/timeline
│   │   └── contact.astro     # Contact form + info
│   └── styles/
│       └── global.css        # Tailwind import + design tokens (@theme)
└── package.json
```

Each `.astro` file in `src/pages/` is exposed as a route based on its file name.

## 🎨 Design

- **Colors, fonts, and spacing** are defined as design tokens in `src/styles/global.css` via
  Tailwind's `@theme` block (e.g. `--color-primary`, `--font-head`). Update tokens there to
  restyle the whole site at once.
- **Images** live in `src/assets/images/` and are rendered with Astro's `<Image>` component
  (`astro:assets`), which generates responsive, modern-format (WebP) variants automatically.
  Hero images are eager-loaded with `fetchpriority="high"`; everything else is lazy-loaded.
- Photos are free-license stock photos from [Unsplash](https://unsplash.com).

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command              | Action                                           |
| :-------------------- | :----------------------------------------------- |
| `npm install`          | Installs dependencies                            |
| `npm run dev`          | Starts local dev server at `localhost:4321`      |
| `npm run build`        | Build the production site to `./dist/`           |
| `npm run preview`      | Preview the build locally, before deploying      |
| `npm run astro ...`    | Run CLI commands like `astro add`, `astro check` |

This project's dev server can also be run in the background:

| Command              | Action                          |
| :-------------------- | :------------------------------- |
| `astro dev --background` | Start the dev server in the background |
| `astro dev stop`         | Stop the background dev server         |
| `astro dev status`       | Check whether it's running             |
| `astro dev logs`         | View dev server logs                   |

## 👀 Want to learn more?

Check out the [Astro docs](https://docs.astro.build) or the
[Tailwind CSS docs](https://tailwindcss.com/docs).

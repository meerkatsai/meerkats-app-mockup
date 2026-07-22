# Meerkats.ai — Product Mockup

Hi-fidelity interactive mockup of the Meerkats.ai growth intelligence product.
Styled entirely with **Tailwind CSS v4**.

## Structure

- **Chat** — conversational entry point, with History, Automations, and Library
- **Core Activities** — Cockpit, CRM (My Queue, All Leads, Team, Performance), Marketing Acquisition, Creative Analysis, Website Conversion, Customer Retention, Discovery
- **Data** — Data Spine (Dashboard, CDP Analytics, Ad Performance, Ingest Events, Google, Meta, Shopify, Attribution), Integrations, Settings

## Styling

Tailwind v4 with a CSS-first theme — there is no hand-written CSS outside the
Tailwind pipeline. Everything compiles from `src/input.css`:

- `@theme` defines the Meerkats design tokens (ember accent, ink text ramp,
  rule borders, semantic good/watch/bad, channel brand colours, and the
  Inter / Source Serif 4 / JetBrains Mono type stack). Each token generates
  utilities — `bg-ember`, `text-ink-500`, `border-rule`, `font-serif`.
- `@layer components` composes those utilities with `@apply` into the repeated
  atoms (buttons, tags, cards, nav items, tables, tiles) so markup stays legible.
- Layout and one-off styling use Tailwind utilities directly in the markup.

```
src/input.css     source of truth — theme tokens + component layer
dist/styles.css   compiled output, committed so the site deploys with no build step
```

## Develop

```bash
npm install
npm run dev      # rebuild dist/styles.css on change
npm run serve    # static server with caching disabled, http://localhost:4710
```

## Build

```bash
npm run build    # minified dist/styles.css
```

## Deploy

Vercel builds the site from source: `vercel.json` runs `npm run build:site`,
which compiles Tailwind and assembles the deployable site into `public/`
(`index.html` + `dist/styles.css`). No framework preset needed — just import
the repo. `dist/styles.css` is also committed so the repo works served
statically (e.g. `npm run serve`) without any build.

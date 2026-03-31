# Vite + React + shadcn + Tailwind CSS

A template starter using Vite, React 19, shadcn/ui, and Tailwind CSS v4.

## Getting Started

```bash
npm install
npm run dev
```

## Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start dev server with HMR |
| `npm run build` | Production build |
| `npm run lint` | Run ESLint |
| `npm run preview` | Preview production build |

## Adding UI Components

This project uses [shadcn/ui](https://ui.shadcn.com/) for pre-built, customizable components:

```bash
npx shadcn@latest add button
npx shadcn@latest add card
npx shadcn@latest add dialog
```

Components are installed to `components/ui/` and can be imported via the `@/` alias:

```jsx
import { Button } from "@/components/ui/button";
```

## Tech Stack

- **[Vite](https://vite.dev/)** — Build tool with HMR
- **[React 19](https://react.dev/)** — UI framework
- **[Tailwind CSS v4](https://tailwindcss.com/)** — Utility-first CSS (configured via `@tailwindcss/vite` plugin)
- **[shadcn/ui](https://ui.shadcn.com/)** — Component library built on Radix UI
- **[Lucide](https://lucide.dev/)** — Icon library
- **[Geist](https://vercel.com/font)** — Font family

## Project Structure

```
src/            → Application source (entry point, styles, assets)
components/ui/  → shadcn UI components
lib/utils.js    → cn() utility (clsx + tailwind-merge)
```

Theme tokens (colors, radii, fonts) are defined as CSS variables in `src/index.css` using Tailwind v4's `@theme inline` — there is no separate `tailwind.config.js`.

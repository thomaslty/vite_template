# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Template starter for a Vite + React 19 + JavaScript + shadcn + Tailwind CSS v4 application.

## Commands

- `npm run dev` — Start dev server with HMR
- `npm run build` — Production build
- `npm run lint` — Run ESLint
- `npm run preview` — Preview production build

## Architecture

**Path aliases:** `@/` resolves to the project root (configured in both `vite.config.js` and `jsconfig.json`).

**Entry flow:** `index.html` → `src/main.jsx` → `src/App.jsx`

**Key directories:**
- `src/` — Application source (components, styles, assets)
- `components/ui/` — shadcn UI components (at project root, not inside `src/`)
- `lib/utils.js` — `cn()` helper combining `clsx` + `tailwind-merge`
- `hooks/` — Custom React hooks (alias configured, directory created on demand)

**Styling:** Tailwind CSS v4 configured via `@tailwindcss/vite` plugin — no `tailwind.config.js`. All theme tokens (colors, radii, fonts) are defined as CSS variables in `src/index.css` using `@theme inline`. Dark mode uses `.dark` class with OKLch color values.

**shadcn setup (`components.json`):**
- Style: `radix-nova`
- JSX (not TSX)
- No React Server Components
- Icon library: `lucide-react`
- Components install to `components/ui/`, utils to `lib/`
- Add components via: `npx shadcn@latest add <component>`

**Component pattern:** shadcn components use `class-variance-authority` (CVA) for variants and Radix UI primitives for accessibility. The `asChild` prop (via Radix `Slot`) allows polymorphic rendering.

# QAudit.dev - Landing Page

## Project Overview

B2B SaaS landing page for QAudit.dev - AI-powered accessibility and security audit platform.

| Item | Value |
|------|-------|
| **Domain** | qaudit.dev |
| **Stack** | SvelteKit 2 + Svelte 5 + TypeScript + TailwindCSS 4 |
| **Adapter** | @sveltejs/adapter-static (self-hosted) |
| **Icons** | lucide-svelte |
| **Repo** | github.com/mihdig/qaudit-dev |

---

## Commands

```bash
# Development
pnpm dev          # Start dev server (usually port 5173)

# Build
pnpm build        # Build static site to /build folder

# Preview
pnpm preview      # Preview production build locally

# Type check
pnpm check        # Run svelte-check
```

---

## Project Structure

```
qaudit-dev/
├── src/
│   ├── app.css              # Design system (ClickUp-inspired)
│   ├── app.html             # HTML template with SEO meta
│   ├── routes/
│   │   ├── +layout.svelte   # Header, Footer, theme toggle
│   │   ├── +layout.ts       # SSR/prerender config
│   │   └── +page.svelte     # Landing page (all sections)
│   └── lib/                 # Shared components (future)
├── static/
│   └── favicon.svg
├── build/                   # Static output (after pnpm build)
├── package.json
├── svelte.config.js
├── vite.config.ts
└── tsconfig.json
```

---

## Design System

### Theme

Dual theme support (light/dark) with toggle. Theme stored in localStorage.

```css
/* Light (default) */
--color-bg: 255 255 255;
--color-text: 15 23 42;

/* Dark (.dark class on html) */
--color-bg: 10 10 20;
--color-text: 248 250 252;
```

### Colors

| Name | CSS Variable | Usage |
|------|--------------|-------|
| Primary | `--color-primary-500` | Success, A11Y green |
| Accent | `--color-accent-500` | Purple, CTAs |
| Pink | `--color-pink-500` | Gradients |
| Error | `--color-error` | Warnings, problems |
| Warning | `--color-warning` | Caution |

### Gradients

```css
--gradient-hero: linear-gradient(135deg, purple → pink);
--gradient-cta: linear-gradient(90deg, purple → pink);
--gradient-text: linear-gradient for text;
```

---

## Svelte 5 Notes

### Runes Mode

This project uses Svelte 5 runes:

```svelte
<script lang="ts">
  let count = $state(0);        // Reactive state
  let doubled = $derived(count * 2);  // Derived

  $effect(() => {               // Side effects
    console.log(count);
  });
</script>
```

### Known Issues

1. **No `class:` directive on components** - Wrap in `<span>` instead:
   ```svelte
   <!-- Wrong -->
   <Icon class:active={isActive} />

   <!-- Correct -->
   <span class={isActive ? 'active' : ''}><Icon /></span>
   ```

2. **Tailwind arbitrary values with `/`** - Move to CSS:
   ```svelte
   <!-- Wrong - Svelte parser fails -->
   <div class="bg-[rgb(var(--color)/0.1)]">

   <!-- Correct - Use CSS class -->
   <div class="my-bg-class">
   ```
   ```css
   .my-bg-class { background: rgb(var(--color) / 0.1); }
   ```

3. **`<svelte:component>` deprecated** - Use dynamic component directly:
   ```svelte
   <!-- Old -->
   <svelte:component this={Icon} />

   <!-- New (Svelte 5) -->
   {@const IconComponent = Icon}
   <IconComponent />
   ```

---

## Landing Page Sections

1. **Hero** - URL input → Scan CTA, animated score ring
2. **Problem** - EAA 2025 urgency, cost/legal/exclusion cards
3. **Features** - 6 cards (WCAG, Security, Speed, Contrast, AI, Reports)
4. **How it Works** - 3 steps with gradient numbers
5. **Pricing** - 4 tiers (Free/$49/$149/$399)
6. **FAQ** - Accordion with 5 questions
7. **CTA** - Final URL input

---

## Deployment

Static site - upload `/build` folder contents to any hosting.

```bash
pnpm build
# Upload build/ to hosting
```

---

## Related Projects

| Project | Path | Description |
|---------|------|-------------|
| A11Y Engine | `../scanners/` | Core scanning engine |
| Dashboard | `../workspace/dashboard-v2/` | Full SaaS dashboard |
| Docs | `./docs/PRODUCT-BRIEF.md` | Product brief |

---
name: wireframe-builder
description: |
  Generate lo-fi wireframes as single HTML files with Tailwind CSS.
  Use when user asks to: create wireframe, sketch page layout, prototype UI,
  design page structure, visualize interface concept, build mockup, or plan
  website/app layout. Supports: landing pages, dashboards, forms, e-commerce,
  admin panels, mobile screens, etc.
---

# Wireframe Builder

Generate lo-fi wireframes as single HTML files using Tailwind CSS with a grayscale `wire-*` palette.

## Quick Start

1. Ask user: page type, main sections, mobile view needed?
2. Copy template from `assets/template.html`
3. Pick components from `references/components.md`
4. Write `.html` file with descriptive name

## HTML Template Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Wireframe - [Page Name]</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            wire: {
              bg: 'hsl(0 0% 100%)',
              surface: 'hsl(0 0% 96%)',
              border: 'hsl(0 0% 88%)',
              muted: 'hsl(0 0% 62%)',
              text: 'hsl(0 0% 26%)',
              dark: 'hsl(0 0% 13%)',
            }
          },
          borderRadius: {
            wire: '0.375rem',
          }
        }
      }
    }
  </script>
  <style type="text/tailwindcss">
    @layer base {
      body {
        @apply bg-wire-bg text-wire-text;
        font-family: system-ui, -apple-system, sans-serif;
      }
    }
  </style>
</head>
<body class="min-h-screen">
  <!-- ========== SECTION NAME ========== -->
  <!-- Content here -->
</body>
</html>
```

## Design Tokens

| Token | Class | Hex | Purpose |
|-------|-------|-----|---------|
| `wire-bg` | `bg-wire-bg` | #ffffff | Page background |
| `wire-surface` | `bg-wire-surface` | #f5f5f5 | Card/section bg |
| `wire-border` | `border-wire-border` | #e0e0e0 | Borders |
| `wire-muted` | `text-wire-muted` | #9e9e9e | Placeholder, icons |
| `wire-text` | `text-wire-text` | #424242 | Body text |
| `wire-dark` | `bg-wire-dark` | #212121 | Headings, primary buttons |

## Core Components

### Image Placeholder
```html
<div class="bg-wire-surface border border-wire-border border-dashed rounded-wire aspect-video flex items-center justify-center">
  <svg class="w-12 h-12 text-wire-muted" fill="currentColor" viewBox="0 0 24 24">
    <path d="M21 19V5c0-1.1-.9-2-2-2H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2zM8.5 13.5l2.5 3.01L14.5 12l4.5 6H5l3.5-4.5z"/>
  </svg>
</div>
```

### Primary Button
```html
<button class="px-4 py-2 bg-wire-dark text-white rounded-wire hover:bg-wire-text transition-colors">
  Button
</button>
```

### Secondary Button
```html
<button class="px-4 py-2 border border-wire-border text-wire-text rounded-wire hover:bg-wire-surface transition-colors">
  Secondary
</button>
```

### Card
```html
<div class="bg-wire-surface border border-wire-border rounded-wire p-4 space-y-3">
  <!-- content -->
</div>
```

### Input
```html
<input type="text" placeholder="Placeholder..."
  class="w-full px-3 py-2 border border-wire-border rounded-wire bg-wire-bg text-wire-text placeholder:text-wire-muted focus:outline-none focus:border-wire-muted">
```

## Interactivity

Use CSS-only where possible:
- Hover: `hover:bg-wire-surface`, `hover:border-wire-muted`
- Focus: `focus:border-wire-muted focus:outline-none`
- Transitions: `transition-colors`
- Accordion: `<details>` / `<summary>` elements

## Layout Patterns

### Container
```html
<div class="max-w-6xl mx-auto px-4">
  <!-- content -->
</div>
```

### Section with Background
```html
<section class="py-16 bg-wire-surface">
  <div class="max-w-6xl mx-auto px-4">
    <!-- content -->
  </div>
</section>
```

### Dashboard (Sidebar + Main)
```html
<div class="flex min-h-screen">
  <aside class="w-64 border-r border-wire-border bg-wire-bg p-4">
    <!-- sidebar -->
  </aside>
  <main class="flex-1 p-6 bg-wire-surface">
    <!-- content -->
  </main>
</div>
```

## Responsive Design

- Mobile-first: start with single column
- Use `md:` breakpoint for tablet/desktop
- Grid: `grid md:grid-cols-2 lg:grid-cols-3 gap-6`
- Hide on mobile: `hidden md:flex`
- Show on mobile: `md:hidden`

## Generation Checklist

- [ ] Use `wire-*` palette only (grayscale)
- [ ] Add HTML comments for sections: `<!-- ===== HEADER ===== -->`
- [ ] Include hover states on interactive elements
- [ ] Make layout responsive with `md:` breakpoints
- [ ] Use semantic HTML (`<header>`, `<main>`, `<section>`, `<footer>`)
- [ ] Test: open in browser, resize to 375px width

## Component Reference

See `references/components.md` for full component library:
- Navigation (header, sidebar, breadcrumbs)
- Hero sections (with image, centered, with form)
- Content (cards, testimonials, pricing, FAQ)
- Forms (login, signup, contact, search)
- Footer (simple, multi-column)
- Tables
- Utility icons (SVG)

## Example Wireframe Types

| Type | Key Sections |
|------|--------------|
| Landing page | Header, Hero, Features, CTA, Footer |
| Dashboard | Sidebar, Stats cards, Table, Charts placeholder |
| E-commerce | Header, Product grid, Filters, Cart |
| Blog | Header, Featured post, Post grid, Sidebar |
| Login/Signup | Centered form card |
| Admin panel | Sidebar, Breadcrumbs, Data table, Pagination |

## File Naming

Use descriptive names:
- `wireframe-landing-page.html`
- `wireframe-dashboard.html`
- `wireframe-checkout-flow.html`

# Wireframe Component Library

Ready-to-use lo-fi components with `wire-*` color palette. Copy and adapt as needed.

---

## Design Tokens

| Token | Class | Purpose |
|-------|-------|---------|
| `wire-bg` | `bg-wire-bg` | Page background (white) |
| `wire-surface` | `bg-wire-surface` | Card/section background (light gray) |
| `wire-border` | `border-wire-border` | Element borders |
| `wire-muted` | `text-wire-muted` | Placeholder text, icons |
| `wire-text` | `text-wire-text` | Body text |
| `wire-dark` | `bg-wire-dark`, `text-wire-dark` | Headings, primary buttons |

---

## Navigation

### Header with Logo + Nav + CTA

```html
<header class="border-b border-wire-border bg-wire-bg sticky top-0 z-50">
  <div class="max-w-6xl mx-auto px-4 py-4 flex items-center justify-between">
    <!-- Logo -->
    <div class="flex items-center gap-2">
      <div class="w-8 h-8 bg-wire-dark rounded-wire"></div>
      <span class="font-semibold text-wire-dark">Brand</span>
    </div>

    <!-- Navigation -->
    <nav class="hidden md:flex items-center gap-6">
      <a href="#" class="text-wire-text hover:text-wire-dark transition-colors">Link</a>
      <a href="#" class="text-wire-text hover:text-wire-dark transition-colors">Link</a>
      <a href="#" class="text-wire-text hover:text-wire-dark transition-colors">Link</a>
    </nav>

    <!-- CTA -->
    <button class="px-4 py-2 bg-wire-dark text-white rounded-wire hover:bg-wire-text transition-colors">
      Action
    </button>
  </div>
</header>
```

### Sidebar Navigation

```html
<aside class="w-64 border-r border-wire-border bg-wire-bg min-h-screen p-4">
  <!-- Logo -->
  <div class="flex items-center gap-2 mb-8">
    <div class="w-8 h-8 bg-wire-dark rounded-wire"></div>
    <span class="font-semibold text-wire-dark">Brand</span>
  </div>

  <!-- Nav items -->
  <nav class="space-y-1">
    <a href="#" class="flex items-center gap-3 px-3 py-2 rounded-wire bg-wire-surface text-wire-dark">
      <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"/>
      </svg>
      Dashboard
    </a>
    <a href="#" class="flex items-center gap-3 px-3 py-2 rounded-wire text-wire-muted hover:bg-wire-surface hover:text-wire-text transition-colors">
      <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"/>
      </svg>
      Users
    </a>
    <a href="#" class="flex items-center gap-3 px-3 py-2 rounded-wire text-wire-muted hover:bg-wire-surface hover:text-wire-text transition-colors">
      <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"/>
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"/>
      </svg>
      Settings
    </a>
  </nav>
</aside>
```

### Breadcrumbs

```html
<nav class="flex items-center gap-2 text-sm text-wire-muted">
  <a href="#" class="hover:text-wire-text transition-colors">Home</a>
  <span>/</span>
  <a href="#" class="hover:text-wire-text transition-colors">Products</a>
  <span>/</span>
  <span class="text-wire-text">Current page</span>
</nav>
```

---

## Hero Sections

### Hero with Image Right

```html
<section class="py-16 md:py-24">
  <div class="max-w-6xl mx-auto px-4">
    <div class="grid md:grid-cols-2 gap-12 items-center">
      <div class="space-y-6">
        <h1 class="text-4xl md:text-5xl font-bold text-wire-dark leading-tight">
          Main headline goes here
        </h1>
        <p class="text-lg text-wire-muted">
          Supporting text that explains the value proposition.
        </p>
        <div class="flex flex-wrap gap-3">
          <button class="px-6 py-3 bg-wire-dark text-white rounded-wire hover:bg-wire-text transition-colors">
            Primary action
          </button>
          <button class="px-6 py-3 border border-wire-border text-wire-text rounded-wire hover:bg-wire-surface transition-colors">
            Secondary action
          </button>
        </div>
      </div>
      <div class="bg-wire-surface border border-wire-border border-dashed rounded-wire aspect-video flex items-center justify-center">
        <svg class="w-16 h-16 text-wire-muted" fill="currentColor" viewBox="0 0 24 24">
          <path d="M21 19V5c0-1.1-.9-2-2-2H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2zM8.5 13.5l2.5 3.01L14.5 12l4.5 6H5l3.5-4.5z"/>
        </svg>
      </div>
    </div>
  </div>
</section>
```

### Hero Centered Minimal

```html
<section class="py-24 md:py-32 text-center">
  <div class="max-w-3xl mx-auto px-4 space-y-6">
    <h1 class="text-4xl md:text-6xl font-bold text-wire-dark">
      Headline here
    </h1>
    <p class="text-xl text-wire-muted">
      Supporting text that explains the value proposition in one or two sentences.
    </p>
    <div class="flex justify-center gap-4">
      <button class="px-8 py-3 bg-wire-dark text-white rounded-wire hover:bg-wire-text transition-colors">
        Get started
      </button>
    </div>
  </div>
</section>
```

### Hero with Signup Form

```html
<section class="py-16 md:py-24">
  <div class="max-w-6xl mx-auto px-4">
    <div class="grid md:grid-cols-2 gap-12 items-center">
      <div class="space-y-6">
        <h1 class="text-4xl md:text-5xl font-bold text-wire-dark leading-tight">
          Headline goes here
        </h1>
        <p class="text-lg text-wire-muted">
          Brief description of the offer.
        </p>
      </div>
      <div class="bg-wire-surface border border-wire-border rounded-wire p-6 space-y-4">
        <h2 class="text-xl font-semibold text-wire-dark">Sign up free</h2>
        <input type="email" placeholder="Email address" class="w-full px-4 py-3 border border-wire-border rounded-wire bg-wire-bg text-wire-text placeholder:text-wire-muted focus:outline-none focus:border-wire-muted">
        <input type="password" placeholder="Password" class="w-full px-4 py-3 border border-wire-border rounded-wire bg-wire-bg text-wire-text placeholder:text-wire-muted focus:outline-none focus:border-wire-muted">
        <button class="w-full px-4 py-3 bg-wire-dark text-white rounded-wire hover:bg-wire-text transition-colors">
          Create account
        </button>
        <p class="text-sm text-wire-muted text-center">
          Already have an account? <a href="#" class="text-wire-text hover:underline">Log in</a>
        </p>
      </div>
    </div>
  </div>
</section>
```

---

## Content Blocks

### Card

```html
<div class="bg-wire-surface border border-wire-border rounded-wire p-6 space-y-4">
  <h3 class="text-lg font-semibold text-wire-dark">Card title</h3>
  <p class="text-wire-muted text-sm">Card description text goes here.</p>
</div>
```

### Card Grid (3 columns)

```html
<div class="grid md:grid-cols-3 gap-6">
  <div class="bg-wire-surface border border-wire-border rounded-wire p-6 space-y-4">
    <div class="w-12 h-12 bg-wire-bg border border-wire-border rounded-wire flex items-center justify-center">
      <svg class="w-6 h-6 text-wire-muted" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"/>
      </svg>
    </div>
    <h3 class="text-lg font-semibold text-wire-dark">Feature</h3>
    <p class="text-wire-muted text-sm">Description text.</p>
  </div>
  <!-- Repeat for more cards -->
</div>
```

### Image Placeholder

```html
<div class="bg-wire-surface border border-wire-border border-dashed rounded-wire aspect-video flex items-center justify-center">
  <svg class="w-12 h-12 text-wire-muted" fill="currentColor" viewBox="0 0 24 24">
    <path d="M21 19V5c0-1.1-.9-2-2-2H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2zM8.5 13.5l2.5 3.01L14.5 12l4.5 6H5l3.5-4.5z"/>
  </svg>
</div>
```

### Avatar Placeholder

```html
<div class="w-12 h-12 bg-wire-surface border border-wire-border rounded-full flex items-center justify-center">
  <svg class="w-6 h-6 text-wire-muted" fill="currentColor" viewBox="0 0 24 24">
    <path d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"/>
  </svg>
</div>
```

### Testimonial

```html
<div class="bg-wire-surface border border-wire-border rounded-wire p-6 space-y-4">
  <p class="text-wire-text italic">"Quote text goes here. Keep it brief and impactful."</p>
  <div class="flex items-center gap-3">
    <div class="w-10 h-10 bg-wire-border rounded-full"></div>
    <div>
      <p class="text-sm font-medium text-wire-dark">Name</p>
      <p class="text-sm text-wire-muted">Title, Company</p>
    </div>
  </div>
</div>
```

### Pricing Card

```html
<div class="bg-wire-bg border border-wire-border rounded-wire p-6 space-y-6">
  <div>
    <h3 class="text-lg font-semibold text-wire-dark">Plan name</h3>
    <p class="text-wire-muted text-sm">Brief description</p>
  </div>
  <div class="flex items-baseline gap-1">
    <span class="text-4xl font-bold text-wire-dark">$29</span>
    <span class="text-wire-muted">/month</span>
  </div>
  <ul class="space-y-3 text-sm">
    <li class="flex items-center gap-2 text-wire-text">
      <svg class="w-5 h-5 text-wire-muted" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/>
      </svg>
      Feature one
    </li>
    <li class="flex items-center gap-2 text-wire-text">
      <svg class="w-5 h-5 text-wire-muted" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/>
      </svg>
      Feature two
    </li>
  </ul>
  <button class="w-full px-4 py-2 bg-wire-dark text-white rounded-wire hover:bg-wire-text transition-colors">
    Choose plan
  </button>
</div>
```

### FAQ Accordion (Pure CSS)

```html
<div class="space-y-2">
  <details class="border border-wire-border rounded-wire">
    <summary class="px-4 py-3 cursor-pointer text-wire-dark font-medium hover:bg-wire-surface transition-colors">
      Question one?
    </summary>
    <div class="px-4 pb-4 text-wire-muted text-sm">
      Answer text goes here.
    </div>
  </details>
  <details class="border border-wire-border rounded-wire">
    <summary class="px-4 py-3 cursor-pointer text-wire-dark font-medium hover:bg-wire-surface transition-colors">
      Question two?
    </summary>
    <div class="px-4 pb-4 text-wire-muted text-sm">
      Answer text goes here.
    </div>
  </details>
</div>
```

---

## Forms

### Input Field

```html
<input type="text" placeholder="Placeholder..."
  class="w-full px-4 py-2 border border-wire-border rounded-wire bg-wire-bg text-wire-text placeholder:text-wire-muted focus:outline-none focus:border-wire-muted">
```

### Input with Label

```html
<div class="space-y-2">
  <label class="text-sm font-medium text-wire-dark">Label</label>
  <input type="text" placeholder="Placeholder..."
    class="w-full px-4 py-2 border border-wire-border rounded-wire bg-wire-bg text-wire-text placeholder:text-wire-muted focus:outline-none focus:border-wire-muted">
</div>
```

### Textarea

```html
<textarea rows="4" placeholder="Message..."
  class="w-full px-4 py-2 border border-wire-border rounded-wire bg-wire-bg text-wire-text placeholder:text-wire-muted focus:outline-none focus:border-wire-muted resize-none"></textarea>
```

### Select

```html
<select class="w-full px-4 py-2 border border-wire-border rounded-wire bg-wire-bg text-wire-text focus:outline-none focus:border-wire-muted">
  <option value="">Select option...</option>
  <option value="1">Option 1</option>
  <option value="2">Option 2</option>
</select>
```

### Checkbox

```html
<label class="flex items-center gap-2 cursor-pointer">
  <input type="checkbox" class="w-4 h-4 border border-wire-border rounded accent-wire-dark">
  <span class="text-sm text-wire-text">Checkbox label</span>
</label>
```

### Login Form

```html
<div class="max-w-sm mx-auto bg-wire-surface border border-wire-border rounded-wire p-6 space-y-4">
  <h2 class="text-xl font-semibold text-wire-dark text-center">Log in</h2>
  <div class="space-y-2">
    <label class="text-sm font-medium text-wire-dark">Email</label>
    <input type="email" placeholder="you@example.com"
      class="w-full px-4 py-2 border border-wire-border rounded-wire bg-wire-bg text-wire-text placeholder:text-wire-muted focus:outline-none focus:border-wire-muted">
  </div>
  <div class="space-y-2">
    <label class="text-sm font-medium text-wire-dark">Password</label>
    <input type="password" placeholder="********"
      class="w-full px-4 py-2 border border-wire-border rounded-wire bg-wire-bg text-wire-text placeholder:text-wire-muted focus:outline-none focus:border-wire-muted">
  </div>
  <button class="w-full px-4 py-2 bg-wire-dark text-white rounded-wire hover:bg-wire-text transition-colors">
    Log in
  </button>
  <p class="text-sm text-wire-muted text-center">
    Don't have an account? <a href="#" class="text-wire-text hover:underline">Sign up</a>
  </p>
</div>
```

### Search Bar

```html
<div class="flex gap-2">
  <input type="search" placeholder="Search..."
    class="flex-1 px-4 py-2 border border-wire-border rounded-wire bg-wire-bg text-wire-text placeholder:text-wire-muted focus:outline-none focus:border-wire-muted">
  <button class="px-4 py-2 bg-wire-dark text-white rounded-wire hover:bg-wire-text transition-colors">
    Search
  </button>
</div>
```

---

## Buttons

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

### Ghost Button

```html
<button class="px-4 py-2 text-wire-text hover:text-wire-dark hover:bg-wire-surface rounded-wire transition-colors">
  Ghost
</button>
```

### Button Group

```html
<div class="flex gap-2">
  <button class="px-4 py-2 bg-wire-dark text-white rounded-wire hover:bg-wire-text transition-colors">Primary</button>
  <button class="px-4 py-2 border border-wire-border text-wire-text rounded-wire hover:bg-wire-surface transition-colors">Secondary</button>
</div>
```

---

## Footer

### Simple Footer

```html
<footer class="border-t border-wire-border py-8">
  <div class="max-w-6xl mx-auto px-4 flex flex-col md:flex-row justify-between items-center gap-4">
    <div class="flex items-center gap-2">
      <div class="w-6 h-6 bg-wire-dark rounded"></div>
      <span class="font-semibold text-wire-dark">Brand</span>
    </div>
    <p class="text-sm text-wire-muted">&copy; 2024 Brand. All rights reserved.</p>
  </div>
</footer>
```

### Multi-column Footer

```html
<footer class="border-t border-wire-border py-12">
  <div class="max-w-6xl mx-auto px-4">
    <div class="grid md:grid-cols-4 gap-8 mb-8">
      <div class="space-y-4">
        <div class="flex items-center gap-2">
          <div class="w-8 h-8 bg-wire-dark rounded-wire"></div>
          <span class="font-semibold text-wire-dark">Brand</span>
        </div>
        <p class="text-sm text-wire-muted">Brief description.</p>
      </div>
      <div>
        <h4 class="font-semibold text-wire-dark mb-4">Column 1</h4>
        <ul class="space-y-2 text-sm text-wire-muted">
          <li><a href="#" class="hover:text-wire-text">Link</a></li>
          <li><a href="#" class="hover:text-wire-text">Link</a></li>
        </ul>
      </div>
      <div>
        <h4 class="font-semibold text-wire-dark mb-4">Column 2</h4>
        <ul class="space-y-2 text-sm text-wire-muted">
          <li><a href="#" class="hover:text-wire-text">Link</a></li>
          <li><a href="#" class="hover:text-wire-text">Link</a></li>
        </ul>
      </div>
      <div>
        <h4 class="font-semibold text-wire-dark mb-4">Column 3</h4>
        <ul class="space-y-2 text-sm text-wire-muted">
          <li><a href="#" class="hover:text-wire-text">Link</a></li>
          <li><a href="#" class="hover:text-wire-text">Link</a></li>
        </ul>
      </div>
    </div>
    <div class="pt-8 border-t border-wire-border text-center text-sm text-wire-muted">
      &copy; 2024 Brand. All rights reserved.
    </div>
  </div>
</footer>
```

---

## Layout Patterns

### Dashboard Layout (Sidebar + Main)

```html
<div class="flex min-h-screen">
  <!-- Sidebar -->
  <aside class="w-64 border-r border-wire-border bg-wire-bg p-4">
    <!-- Sidebar content -->
  </aside>

  <!-- Main content -->
  <main class="flex-1 p-6 bg-wire-surface">
    <!-- Page content -->
  </main>
</div>
```

### Container with Max Width

```html
<div class="max-w-6xl mx-auto px-4">
  <!-- Content -->
</div>
```

### Section with Background

```html
<section class="py-16 bg-wire-surface">
  <div class="max-w-6xl mx-auto px-4">
    <!-- Content -->
  </div>
</section>
```

---

## Tables

### Simple Table

```html
<div class="border border-wire-border rounded-wire overflow-hidden">
  <table class="w-full">
    <thead class="bg-wire-surface">
      <tr>
        <th class="px-4 py-3 text-left text-sm font-medium text-wire-dark">Column</th>
        <th class="px-4 py-3 text-left text-sm font-medium text-wire-dark">Column</th>
        <th class="px-4 py-3 text-left text-sm font-medium text-wire-dark">Column</th>
      </tr>
    </thead>
    <tbody class="divide-y divide-wire-border">
      <tr class="hover:bg-wire-surface transition-colors">
        <td class="px-4 py-3 text-sm text-wire-text">Data</td>
        <td class="px-4 py-3 text-sm text-wire-text">Data</td>
        <td class="px-4 py-3 text-sm text-wire-text">Data</td>
      </tr>
      <tr class="hover:bg-wire-surface transition-colors">
        <td class="px-4 py-3 text-sm text-wire-text">Data</td>
        <td class="px-4 py-3 text-sm text-wire-text">Data</td>
        <td class="px-4 py-3 text-sm text-wire-text">Data</td>
      </tr>
    </tbody>
  </table>
</div>
```

---

## Utility Icons (SVG)

### Image Icon
```html
<svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
  <path d="M21 19V5c0-1.1-.9-2-2-2H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2zM8.5 13.5l2.5 3.01L14.5 12l4.5 6H5l3.5-4.5z"/>
</svg>
```

### User Icon
```html
<svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
  <path d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"/>
</svg>
```

### Check Icon
```html
<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/>
</svg>
```

### Menu Icon (Hamburger)
```html
<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
</svg>
```

### Close Icon
```html
<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/>
</svg>
```

### Arrow Right Icon
```html
<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
</svg>
```

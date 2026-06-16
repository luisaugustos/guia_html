# Accessibility in HTML (WCAG and ARIA)

**Web accessibility** means creating websites that everyone can use, including people with disabilities. It's a right, a legal responsibility, and good engineering practice.

## Why is accessibility important?

1. **Inclusion** — Benefits ~15% of global population with disabilities
2. **Legal** — Many countries require accessibility (ADA in USA, AODA in Canada)
3. **SEO** — Google rewards accessible sites
4. **Business** — Reaches more users
5. **Quality** — More semantic and maintainable code

## WCAG Guidelines (Web Content Accessibility Guidelines)

WCAG 2.1 defines three levels:

- **A** — Basic compliance
- **AA** — Intermediate compliance (recommended)
- **AAA** — Maximum compliance

Core principles (POUR):

1. **P**erceptible — Information perceivable
2. **O**perable — Keyboard navigation
3. **U**nderstandable — Understandable content
4. **R**obust — Compatible with assistive technologies

## Correct HTML semantics

The first step is using **proper HTML tags**:

```html
<!-- ✓ CORRECT: Semantic -->
<header>
  <nav>
    <ul>
      <li><a href="/home">Home</a></li>
      <li><a href="/about">About</a></li>
    </ul>
  </nav>
</header>

<main>
  <article>
    <h1>Article title</h1>
    <p>Content...</p>
  </article>
</main>

<footer>
  <p>&copy; 2026</p>
</footer>

<!-- ✗ INCORRECT: Generic divs -->
<div class="header">
  <div class="nav">
    <div class="menu">...</div>
  </div>
</div>
```

**Important semantic tags:**
- `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<aside>`, `<footer>`
- `<h1>` to `<h6>` for headings (in order)
- `<label>` for form fields
- `<table>` for tabular data

## `alt` attributes on images

The `alt` attribute is **required** and critical:

```html
<!-- ✓ GOOD: Meaningful description -->
<img src="sales-chart.png" alt="Q1 2026 sales chart showing 15% increase">

<!-- ✓ ACCEPTABLE: Decorative image -->
<img src="divider-line.png" alt="">

<!-- ✗ BAD: Missing alt -->
<img src="chart.png">

<!-- ✗ BAD: Redundant -->
<img src="photo.jpg" alt="photo"> <!-- Not useful -->
```

**Rule:** If image communicates information, describe what it says. If purely decorative, use `alt=""`.

## ARIA (Accessible Rich Internet Applications)

ARIA provides **attributes** to describe role, state, and properties:

### ARIA Roles

```html
<!-- Define element role -->
<div role="button" onclick="doSomething()">Click here</div>

<div role="alert">Important warning!</div>

<div role="navigation">...</div>

<div role="search">...</div>
```

### Labels and descriptions

```html
<!-- aria-label: invisible label -->
<button aria-label="Close menu">×</button>

<!-- aria-labelledby: reference another element -->
<h2 id="dialog-title">Confirm action</h2>
<div role="dialog" aria-labelledby="dialog-title">
  Are you sure?
</div>

<!-- aria-describedby: additional description -->
<input type="password" aria-describedby="pwd-hint">
<p id="pwd-hint">Minimum 8 characters, include numbers</p>
```

### State properties

```html
<!-- aria-expanded: expanded/collapsed -->
<button aria-expanded="false" aria-controls="menu">Menu</button>
<div id="menu" hidden>Options...</div>

<!-- aria-current: current page -->
<nav>
  <a href="/home" aria-current="page">Home</a>
  <a href="/about">About</a>
</nav>

<!-- aria-disabled: disabled -->
<button aria-disabled="true">Not available</button>

<!-- aria-live: live updates -->
<div aria-live="polite" aria-atomic="true">
  New messages loaded...
</div>
```

## Keyboard navigation

### Tab order

```html
<!-- Use tabindex=0 for non-standard interactive elements -->
<div tabindex="0" role="button">Clickable</div>

<!-- Avoid positive tabindex (breaks natural order) -->
<!-- ✗ BAD: tabindex="1", tabindex="2", etc. -->

<!-- To remove from keyboard navigation -->
<div tabindex="-1">Not keyboard navigable</div>
```

### Focus visibility

```html
<!-- Ensure focus is visible -->
<style>
  button:focus {
    outline: 2px solid blue;
    outline-offset: 2px;
  }
</style>

<!-- ✗ BAD: Remove outline without alternative -->
button:focus {
  outline: none; /* Never do this alone */
}
```

## Color contrast

WCAG AA requires:
- **Normal:** ratio 4.5:1
- **Large:** ratio 3:1

```html
<!-- ✓ GOOD: Sufficient contrast -->
<p style="color: #000; background: #fff;">High contrast text</p>

<!-- ✗ BAD: Insufficient contrast -->
<p style="color: #ccc; background: #ddd;">Hard to read</p>
```

## Heading structure

```html
<!-- ✓ CORRECT: Logical hierarchy -->
<h1>Main page title</h1>

<section>
  <h2>Section 1</h2>
  <h3>Subsection 1.1</h3>
  <h3>Subsection 1.2</h3>
</section>

<section>
  <h2>Section 2</h2>
</section>

<!-- ✗ INCORRECT: Skipped levels -->
<h1>Title</h1>
<h3>Direct jump to h3</h3> <!-- Confusing for screen readers -->
```

## Screen readers

Blind/visually impaired users use readers like:
- NVDA (free, Windows)
- JAWS (Windows)
- VoiceOver (macOS/iOS)
- TalkBack (Android)

**Tip:** test your site with NVDA to verify accessibility.

## Basic accessibility checklist

- ✅ Use semantic HTML tags
- ✅ All visual content has `alt` attribute
- ✅ Forms have `<label>` elements
- ✅ Color contrast >= 4.5:1
- ✅ Keyboard navigable (Tab, Enter, Escape)
- ✅ Focus visible on all interactive elements
- ✅ Headings in hierarchical order
- ✅ Videos have captions and descriptions
- ✅ Links have descriptive text (not "click here")
- ✅ Site works without JavaScript

---

In upcoming topics you'll learn:
1. ARIA in depth
2. Accessibility testing
3. Audit tools
4. Common accessible patterns

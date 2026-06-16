# Advanced Attributes (Data Attributes and Global)

**Advanced attributes** allow you to store custom data, control special behaviors, and enhance page interactivity without complex JavaScript.

## Data attributes (`data-*`)

Data attributes let you **store custom information** in HTML elements, accessible from JavaScript:

```html
<!-- Element with custom data -->
<div class="product" 
     data-id="12345" 
     data-price="29.99" 
     data-available="true">
  Gaming Laptop
</div>

<button data-action="save" data-confirmation="true">
  Save changes
</button>
```

### Access from JavaScript

```javascript
// Get data
const product = document.querySelector('.product');
console.log(product.dataset.id);        // "12345"
console.log(product.dataset.price);     // "29.99"
console.log(product.dataset.available); // "true"

// Set data
product.dataset.status = 'sold';
```

### Common use cases

```html
<!-- E-commerce: product information -->
<div class="cart-item" 
     data-sku="PROD-001" 
     data-quantity="2" 
     data-total="59.98">
  <h3>Product A</h3>
  <p>$29.99 x 2</p>
</div>

<!-- Forms: custom validation -->
<input type="text" 
       data-validate="email" 
       data-required="true"
       placeholder="Your email">

<!-- Galleries: image information -->
<img src="photo.jpg" 
     alt="Description" 
     data-author="John Garcia"
     data-year="2026"
     data-license="CC-BY-4.0">

<!-- Animations: configuration -->
<div class="animation" 
     data-duration="2000" 
     data-delay="500"
     data-repeat="infinite">
  Animated content
</div>
```

## Global attributes

**Global attributes** work on **any HTML element**:

### `id` — Unique identifier

```html
<!-- Define unique identifier for element -->
<h1 id="main-title">Welcome</h1>

<!-- Use in internal links -->
<a href="#main-title">Go to title</a>

<!-- Use in JavaScript -->
<button onclick="document.getElementById('main-title').style.color='red';">
  Change color
</button>
```

**Rules:**
- ✅ Unique identifier per page
- ✅ No spaces or special characters
- ✅ Start with letter or underscore

### `class` — CSS classes

```html
<!-- Apply multiple classes -->
<div class="container main large">
  Content with multiple styles
</div>

<!-- CSS -->
<style>
  .container { padding: 20px; }
  .main { font-weight: bold; }
  .large { width: 100%; }
</style>
```

### `style` — Inline styles (not recommended)

```html
<!-- Direct styles (avoid when possible) -->
<p style="color: blue; font-size: 18px;">
  Paragraph with inline styles
</p>

<!-- ✓ BETTER: Use classes in external CSS -->
<p class="highlighted-text">
  Paragraph with class
</p>
```

### `title` — Information on hover

```html
<!-- Tooltip on hover -->
<button title="Click to save">Save</button>

<img src="photo.jpg" 
     alt="Description" 
     title="Photo from USAL (2026)">

<abbr title="General Assembly">GA</abbr>
```

### `hidden` — Hide elements

```html
<!-- Hide element without removing from DOM -->
<div hidden>
  Hidden content (invisible but exists in HTML)
</div>

<!-- Show with JavaScript -->
<button onclick="document.querySelector('div').hidden = false;">
  Show
</button>
```

### `tabindex` — Keyboard navigation order

```html
<!-- Element focusable by keyboard -->
<div tabindex="0" role="button">Interactive element</div>

<!-- Elements not keyboard navigable (e.g., decorative) -->
<span tabindex="-1">Non-navigable element</span>

<!-- AVOID: Positive order breaks natural flow -->
<!-- ✗ BAD: <div tabindex="1">...</div> -->
```

### `contenteditable` — Edit content

```html
<!-- Allow content editing -->
<div contenteditable="true">
  This text can be edited by clicking
</div>

<!-- Read-only -->
<div contenteditable="false">
  This text cannot be edited
</div>
```

### `spellcheck` — Spell checking

```html
<!-- Enable spell checking -->
<textarea spellcheck="true" 
          placeholder="Type here..."></textarea>

<!-- Disable spell checking -->
<input type="text" spellcheck="false">
```

### `draggable` — Draggable

```html
<!-- Make element draggable -->
<div draggable="true">
  I can be dragged
</div>

<img src="image.jpg" draggable="true" alt="Draggable image">
```

### `lang` — Language

```html
<!-- Specify language for accessibility and SEO -->
<html lang="en">
  <head>
    <title>My page</title>
  </head>
  <body>
    <p>Text in English</p>
    <p lang="es">Texto en español</p>
    <p lang="fr">Texte en français</p>
  </body>
</html>
```

### `dir` — Text direction

```html
<!-- Right-to-left text -->
<div dir="rtl">
  النص العربي يكتب من اليمين إلى اليسار
</div>

<!-- Left-to-right text (default) -->
<div dir="ltr">
  Text is read from left to right
</div>
```

## Special attributes

### `aria-*` — Accessibility (ARIA)

```html
<!-- Define element role -->
<div role="button" aria-pressed="false">
  Simulated button
</div>

<!-- Label for screen readers -->
<button aria-label="Close menu">×</button>

<!-- Additional description -->
<input aria-describedby="pwd-hint">
<p id="pwd-hint">Minimum 8 characters</p>
```

### `rel` — Relationship with external resources

```html
<!-- Link to stylesheet -->
<link rel="stylesheet" href="styles.css">

<!-- Favicon -->
<link rel="icon" href="favicon.ico">

<!-- Preload resource -->
<link rel="preload" href="font.woff2" as="font">

<!-- Link to alternate version -->
<link rel="alternate" href="/es/" hreflang="es">
```

## Advanced attributes checklist

- ✅ Use `data-*` for custom data
- ✅ Unique `id` per page
- ✅ `class` for CSS styles (not inline `style`)
- ✅ `title` for additional information
- ✅ `hidden` to hide elements
- ✅ `tabindex="0"` for interactive elements
- ✅ `lang` for multiple languages
- ✅ `aria-*` for accessibility
- ✅ `rel` for correct relationships

---

In the next chapter you'll learn about advanced **Meta Tags** for SEO, social media, and progressive web apps.

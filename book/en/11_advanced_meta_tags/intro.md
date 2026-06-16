# Advanced Meta Tags (Open Graph, Twitter Cards, PWA)

**Advanced meta tags** control how your pages appear on **social media**, **search engines**, and **progressive web apps**.

## Open Graph (OG)

Open Graph lets you control what **image, title, and description** appear when your page is shared on social media.

### Open Graph meta tags

```html
<head>
  <!-- Page title (for OG) -->
  <meta property="og:title" content="HTML Guide for Engineering">
  
  <!-- Description (for OG) -->
  <meta property="og:description" content="Learn HTML from scratch with practical examples">
  
  <!-- Image displayed (recommended 1200x630px) -->
  <meta property="og:image" content="https://example.com/cover.jpg">
  
  <!-- Page URL -->
  <meta property="og:url" content="https://example.com/html">
  
  <!-- Content type -->
  <meta property="og:type" content="website">
  
  <!-- Language (optional) -->
  <meta property="og:locale" content="en_US">
</head>
```

### Complete example

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>HTML Guide | USAL</title>
  
  <!-- Standard SEO meta -->
  <meta name="description" content="Interactive HTML tutorial for Computer Engineering students">
  <meta name="keywords" content="HTML5, web development, tutorial">
  
  <!-- Open Graph for social media -->
  <meta property="og:title" content="HTML Guide for Computer Engineering">
  <meta property="og:description" content="Interactive HTML5 tutorial for USAL students">
  <meta property="og:image" content="https://guide.example.com/og-image.jpg">
  <meta property="og:url" content="https://guide.example.com/html">
  <meta property="og:type" content="website">
  <meta property="og:site_name" content="HTML Guide USAL">
  
  <!-- Twitter Card -->
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:title" content="HTML Guide for Engineering">
  <meta name="twitter:description" content="Learn HTML from scratch">
  <meta name="twitter:image" content="https://guide.example.com/twitter-image.jpg">
  <meta name="twitter:site" content="@usal">
</head>
<body>
  <!-- Content... -->
</body>
</html>
```

## Twitter Cards

**Twitter Cards** control how your content appears on Twitter/X when shared.

### Card types

#### `summary` — Simple card

```html
<meta name="twitter:card" content="summary">
<meta name="twitter:title" content="My article">
<meta name="twitter:description" content="Brief description">
<meta name="twitter:image" content="https://example.com/image.jpg">
```

#### `summary_large_image` — Large image

```html
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="My article">
<meta name="twitter:description" content="Brief description">
<meta name="twitter:image" content="https://example.com/large-image.jpg">
```

#### `player` — For video/audio

```html
<meta name="twitter:card" content="player">
<meta name="twitter:player" content="https://example.com/player">
<meta name="twitter:player:width" content="550">
<meta name="twitter:player:height" content="310">
```

### Additional attributes

```html
<!-- Twitter username -->
<meta name="twitter:creator" content="@your_user">
<meta name="twitter:site" content="@site_name">

<!-- Recommended image dimensions -->
<!-- summary: 200x200px minimum, 1MB max -->
<!-- summary_large_image: 506x506px minimum, 1MB max -->
```

## PWA (Progressive Web App)

**PWAs** are web apps that work offline and can be installed on devices.

### Manifest.json

```json
{
  "name": "HTML Guide",
  "short_name": "HTML",
  "description": "Interactive HTML tutorial for engineering",
  "start_url": "/",
  "display": "standalone",
  "background_color": "#ffffff",
  "theme_color": "#1976d2",
  "icons": [
    {
      "src": "/icon-192x192.png",
      "sizes": "192x192",
      "type": "image/png"
    },
    {
      "src": "/icon-512x512.png",
      "sizes": "512x512",
      "type": "image/png"
    }
  ]
}
```

### Link manifest in HTML

```html
<head>
  <link rel="manifest" href="/manifest.json">
  
  <!-- Status bar color on mobile -->
  <meta name="theme-color" content="#1976d2">
  
  <!-- Icon for Apple -->
  <link rel="apple-touch-icon" href="/icon-180x180.png">
</head>
```

### Service Worker

```html
<!-- Register Service Worker -->
<script>
  if ('serviceWorker' in navigator) {
    navigator.serviceWorker.register('/sw.js')
      .then(() => console.log('SW registered'))
      .catch(err => console.log('Error:', err));
  }
</script>
```

## Mobile meta tags

```html
<!-- Viewport (essential for responsive) -->
<meta name="viewport" content="width=device-width, initial-scale=1">

<!-- Allow installation on home screen -->
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="HTML Guide">

<!-- Address bar color in Android -->
<meta name="theme-color" content="#1976d2">

<!-- Disable zoom (use carefully) -->
<!-- <meta name="viewport" content="user-scalable=no"> -->
```

## Complete SEO meta tags

```html
<head>
  <!-- Basic meta -->
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  
  <!-- SEO -->
  <title>HTML Guide | USAL</title>
  <meta name="description" content="HTML tutorial for Computer Engineering">
  <meta name="keywords" content="HTML, web, tutorial, USAL">
  <meta name="author" content="Luis Augusto Silva">
  
  <!-- Open Graph -->
  <meta property="og:title" content="HTML Guide">
  <meta property="og:description" content="Interactive tutorial">
  <meta property="og:image" content="https://example.com/og.jpg">
  <meta property="og:url" content="https://example.com">
  <meta property="og:type" content="website">
  
  <!-- Twitter -->
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:title" content="HTML Guide">
  <meta name="twitter:description" content="Interactive tutorial">
  <meta name="twitter:image" content="https://example.com/twitter.jpg">
  
  <!-- PWA -->
  <link rel="manifest" href="/manifest.json">
  <meta name="theme-color" content="#1976d2">
  
  <!-- Favicon -->
  <link rel="icon" href="/favicon.ico">
  <link rel="apple-touch-icon" href="/apple-icon.png">
  
  <!-- Canonical (for duplicates) -->
  <link rel="canonical" href="https://example.com/html">
</head>
```

## Validate meta tags

**Useful tools:**

- **Open Graph Debugger** — https://developers.facebook.com/tools/debug/
- **Twitter Card Validator** — https://cards-dev.twitter.com/validator
- **Google Search Console** — https://search.google.com/search-console/
- **Lighthouse** (in DevTools) — Audit PWA

## Advanced meta tags checklist

- ✅ `og:title`, `og:description`, `og:image` for social media
- ✅ OG image: 1200x630px minimum
- ✅ Twitter Card type appropriate (`summary_large_image` recommended)
- ✅ `manifest.json` for PWA
- ✅ `theme-color` for mobile
- ✅ `viewport` for responsive
- ✅ `canonical` if duplicates exist
- ✅ `description` for SEO
- ✅ Validate with official tools

---

With these advanced meta tags, your page will have better **social media visibility**, **better SEO**, and can function as a **progressive web app**. Congratulations, you've completed the HTML guide!

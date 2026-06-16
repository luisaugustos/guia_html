# The HTML Document: Internal Structure

Every HTML page has a specific internal structure. Although you only see the content of the `<body>` in the browser, there's much more happening in the document's head (`<head>`).

## Complete structure of an HTML document

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Title of my page</title>
    <link rel="icon" href="favicon.ico">
    <meta name="description" content="Brief description">
  </head>
  <body>
    <h1>Visible content here</h1>
  </body>
</html>
```

## What is the `<head>`?

The `<head>` is the **document header**. It contains:

- **Metadata** — information about the page
- **Links** — to stylesheets, fonts, icons
- **Title** — what appears in the browser tab
- **Scripts** — JavaScript code
- **Instructions** — how the browser should interpret the content

The content of the `<head>` **doesn't appear on the page**, only the `<body>` does.

## The `lang` attribute

Always specify the main language:

```html
<html lang="en">  <!-- English -->
<html lang="es">  <!-- Spanish -->
<html lang="fr">  <!-- French -->
```

This is important for:
- Search engines (SEO)
- Screen readers (accessibility)
- Browser spell checkers

## Meta charset

Specifies the **character encoding** of the document:

```html
<meta charset="UTF-8">
```

UTF-8 is the modern standard and supports all languages and symbols. **Always use UTF-8**.

## Meta viewport

Makes the page **responsive** (adapts to mobile screens):

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Without this, your page would look bad on mobile devices.

## Page title

```html
<title>My First Website</title>
```

The title appears in:
- The browser tab
- Search results
- Browser history

**Important rule**: each page should have a unique and descriptive title.

## Favicon

The **favicon** is the small icon that appears in the browser tab:

```html
<link rel="icon" href="favicon.ico">
```

You can use:
- `favicon.ico` — traditional format
- `favicon.png` — modern format
- `favicon.svg` — vector (recommended)

## Meta description

A brief description of your page that appears in search results:

```html
<meta name="description" content="Learn HTML from scratch. A practical guide for computer engineers.">
```

It should be 150-160 characters to appear complete in Google.

## Meta tags for social media

Control how your page appears when shared on social media:

```html
<meta property="og:title" content="My First Website">
<meta property="og:description" content="Brief description">
<meta property="og:image" content="image.png">
<meta property="og:url" content="https://example.com">
```

These are **Open Graph** tags used by Facebook, Twitter, LinkedIn, etc.

## Linking stylesheets

```html
<link rel="stylesheet" href="styles.css">
```

By convention, CSS links go in the `<head>`.

## Scripts

```html
<script src="script.js"></script>
```

Although they can technically go in the `<head>` or at the end of the `<body>`, they're usually placed at the end of the `<body>` so the page loads faster.

The following chapters will dive deeper into each of these elements.

# Charset (Character Encoding)

The `charset` attribute defines which **character encoding** your HTML document uses. It's essential for browsers to correctly interpret text in different languages and special characters.

## What is charset?

The charset specifies the **character encoding** used by the file:

- **UTF-8** — Universal charset (recommended, includes all languages)
- **ISO-8859-1** — Latin characters
- **Windows-1252** — Windows characters
- **ASCII** — Basic English characters

## Declare charset in `<head>`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Page</title>
</head>
<body>
  <h1>Hello, world!</h1>
</body>
</html>
```

**Important rule:** The `<meta charset>` must be the **first element** inside `<head>` so the browser processes it immediately.

```html
<!-- ✓ CORRECT: Meta charset is first -->
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Page</title>
</head>

<!-- ✗ INCORRECT: Meta charset is not first -->
<head>
  <title>Page</title>
  <meta charset="UTF-8">
</head>
```

## UTF-8: The universal standard

**UTF-8** is the default and recommended charset:

✅ Supports **all world languages**
✅ Compatible with **special characters**
✅ Efficient in **file size**
✅ Modern web standard

### Examples of supported Unicode characters

```html
<meta charset="UTF-8">

<!-- Spanish -->
<p>Accents: á, é, í, ó, ú, ñ</p>

<!-- French -->
<p>Characters: ç, è, ê, ë</p>

<!-- German -->
<p>Umlauts: ä, ö, ü, ß</p>

<!-- Mathematical characters and symbols -->
<p>Symbols: © ® ™ € ¥ ± × ÷ ≠ ≤ ≥</p>

<!-- Emoji (also UTF-8) -->
<p>Emojis and special symbols supported</p>
```

## Common problems without correct charset

Without declaring `charset="UTF-8"`, the browser may misinterpret characters:

```html
<!-- ✗ BAD: Without meta charset, accented characters may appear as:
    â€œHelloâ€? instead of "Hello"
-->
<head>
  <title>Page without charset</title>
</head>

<!-- ✓ GOOD: With charset, everything displays correctly -->
<head>
  <meta charset="UTF-8">
  <title>Correct page</title>
</head>
```

## HTML entities for special characters

If for some reason you need special characters without UTF-8, use **HTML entities**:

| Character | Entity | Description |
|---|---|---|
| `©` | `&copy;` | Copyright |
| `®` | `&reg;` | Registered trademark |
| `™` | `&trade;` | Trademark |
| `€` | `&euro;` | Euro |
| `¥` | `&yen;` | Yen |
| `£` | `&pound;` | Pound |
| `§` | `&sect;` | Section |
| `¶` | `&para;` | Paragraph |
| `†` | `&dagger;` | Dagger |
| `‡` | `&Dagger;` | Double dagger |

**Example:**

```html
<p>Copyright &copy; 2026 University of Salamanca</p>
<!-- Will display as: Copyright © 2026 University of Salamanca -->
```

## Save files as UTF-8

Make sure your **text editor** saves files in **UTF-8** encoding:

### VS Code
1. Click `UTF-8` in the bottom right corner
2. Select `Save with Encoding...` → `UTF-8`

### Other editors
- **Notepad++** — Encoding → Encode in UTF-8
- **Sublime Text** — File → Save with Encoding → UTF-8
- **Atom** — File → Save As → Encoding: UTF-8

## Charset checklist

- ✅ `<meta charset="UTF-8">` is the first element in `<head>`
- ✅ File saved as **UTF-8** in your editor
- ✅ Accented characters display correctly in browser
- ✅ Emoji and special symbols work
- ✅ Don't use obsolete charsets (ISO-8859-1, Windows-1252)

---

With charset properly configured, your page will display any language and special character correctly. In the next topic you'll learn about other important meta attributes.

# HTML Fundamental Concepts

In this section you will learn the basic concepts you need to understand to work with HTML. It's not complicated, but it's important to grasp these ideas well from the beginning.

## What is a tag?

A **tag** is the basic unit of HTML. It's code that tells the browser how to display or interpret content.

A typical tag has this structure:

```html
<tagname>content</tagname>
```

Example:
```html
<p>This is a paragraph.</p>
```

Here, `<p>` is the **opening tag**, `This is a paragraph.` is the **content**, and `</p>` is the **closing tag**. The browser interprets this as a paragraph.

## Self-closing tags

Some tags have no content and close themselves. They're called **empty tags** or **self-closing tags**:

```html
<img src="image.png" alt="Description">
<br>
<input type="text">
```

These tags don't need a separate closing tag.

## What are attributes?

**Attributes** are additional properties that add information to a tag. They're placed inside the opening tag.

```html
<img src="image.png" alt="Image description">
```

In this example:
- `src` is the attribute that specifies the **path** to the image
- `alt` is the attribute that provides **alternative text** if the image can't be loaded

Attributes always have the form `name="value"`.

## Nesting

Tags can contain other tags. This is called **nesting**. Example:

```html
<div>
  <h1>Main Title</h1>
  <p>This paragraph is inside the div.</p>
</div>
```

Here, `<h1>` and `<p>` are **nested** inside the `<div>`. Order matters: the tag that opens first must close last.

## Basic structure of an HTML document

Every HTML page has a minimal structure:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page title</title>
  </head>
  <body>
    <h1>Content here</h1>
  </body>
</html>
```

- `<!DOCTYPE html>` — tells the browser it's an HTML5 document
- `<html>` — the root tag that contains everything
- `<head>` — contains information about the page (not visible in the browser)
- `<body>` — contains the visible content of the page

## Comments

**Comments** are annotations in the code that the browser ignores. They're useful for documenting your work:

```html
<!-- This is a comment -->
<p>This text is visible</p>
<!-- You can explain here what this section does -->
```

Comments don't appear on the page, only in the source code.

## Special characters

Sometimes you need to display special characters in HTML. Use **HTML entities**:

| Character | Code | Use |
|---|---|---|
| `<` | `&lt;` | Less than |
| `>` | `&gt;` | Greater than |
| `&` | `&amp;` | Ampersand |
| `"` | `&quot;` | Double quotes |
| `'` | `&#39;` | Single quotes |
| `©` | `&copy;` | Copyright symbol |
| `€` | `&euro;` | Euro symbol |

Example:
```html
<p>The price is &lt; 10€ and the formula is E &gt; mc²</p>
```

Following chapters will cover each of these concepts in depth.

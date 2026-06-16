# Links and Hyperlinks

**Links** are the essence of the web. Without them, there would be no way to navigate from one page to another. In this section you'll learn how to create and manage links correctly.

## The `<a>` tag

The `<a>` tag (anchor) creates a hyperlink. Its main attribute is `href` (Hypertext REFerence):

```html
<a href="https://example.com">Click here</a>
```

The text between `<a>` and `</a>` is what the user sees and can click on.

## URLs vs. Paths

There are two ways to specify destinations:

### Absolute URLs
Complete web address:
```html
<a href="https://www.google.com">Google</a>
<a href="http://example.com/page.html">External page</a>
```

### Relative Paths
Paths within your own site:
```html
<a href="page.html">Page in same directory</a>
<a href="folder/page.html">Page in a folder</a>
<a href="../page.html">Page in parent folder</a>
<a href="/">Home page</a>
```

## Link attributes

| Attribute | Use | Example |
|---|---|---|
| `href` | Link destination | `href="page.html"` |
| `target` | Where to open | `target="_blank"` (new tab) |
| `title` | Text on hover | `title="See more information"` |
| `rel` | Relation to destination | `rel="noopener noreferrer"` |
| `download` | Download file | `download="file.pdf"` |

## Open in new tab

```html
<a href="https://example.com" target="_blank" rel="noopener noreferrer">
  Open in new tab
</a>
```

The `rel="noopener noreferrer"` attribute is important for security.

## Internal links within the page

Use `id` to create links to sections:

```html
<!-- Create a destination -->
<h2 id="section-2">Section 2</h2>

<!-- Create a link to that destination -->
<a href="#section-2">Go to Section 2</a>
```

## Download files

```html
<a href="document.pdf" download>Download PDF</a>
<a href="image.png" download="my-image.png">Download with different name</a>
```

## Email and phone

```html
<!-- Email link -->
<a href="mailto:user@example.com">Send email</a>

<!-- Phone link -->
<a href="tel:+34123456789">Call</a>

<!-- Email with parameters (add ?subject=topic to href) -->
<a href="mailto:user@example.com">Send inquiry</a>
```

## Best practices

1. **Descriptive text** — use text that explains where the link goes, not "click here"
2. **Clear structure** — links should be easy to identify
3. **URL validation** — verify that links work
4. **Accessibility** — links must be navigable with keyboard

## Difference between paths

Imagine this structure:
```
site/
  ├── index.html
  ├── page1.html
  └── folder/
      └── page2.html
```

From `folder/page2.html`:
- `../index.html` → go up one folder, access index.html
- `../page1.html` → go up one folder, access page1.html
- `./file.html` → in current folder
- `../../file.html` → go up two folders

The following chapters will teach you more about paths and how to organize them correctly.

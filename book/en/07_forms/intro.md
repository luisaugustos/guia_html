# Forms in HTML

**Forms** are one of the most important HTML elements. They allow users to interact with your website by sending data to the server. Everything from login to searches goes through forms.

## Why are forms important?

Forms are the primary way to:
- ✅ Collect user information
- ✅ Process data (login, registration, search)
- ✅ Enable bidirectional interaction
- ✅ Improve user experience
- ✅ Validate data before sending to server

## Basic form structure

A simple form has this structure:

```html
<form action="/process" method="POST">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required>
  
  <button type="submit">Send</button>
</form>
```

## Main components

A complete form includes:

### 1. **The `<form>` tag**
```html
<form action="/process" method="POST">
  <!-- Form content -->
</form>
```
- `action` — URL where data is sent
- `method` — HTTP method: `GET` or `POST`

### 2. **Input fields**
```html
<input type="text" name="username">
<textarea name="message"></textarea>
<select name="country">
  <option>Spain</option>
</select>
```

### 3. **`<label>` tags**
```html
<label for="email">Email:</label>
<input type="email" id="email" name="email">
```
- Make the form accessible
- Increase clickable area
- Describe the field

### 4. **Buttons**
```html
<button type="submit">Send</button>
<button type="reset">Clear</button>
<button type="button">Action</button>
```

## Important `<form>` attributes

| Attribute | Use | Example |
|-----------|-----|---------|
| `action` | Destination URL | `action="/login"` |
| `method` | GET or POST | `method="POST"` |
| `enctype` | Encoding (for files) | `enctype="multipart/form-data"` |
| `name` | Form name | `name="login-form"` |
| `autocomplete` | Autocomplete | `autocomplete="on"` |
| `novalidate` | No HTML5 validation | `novalidate` |

## GET vs POST

### **GET**
- Sends data in the URL
- Visible in address bar
- Limited to ~2000 characters
- Use: searches, filters

```html
<form action="/search" method="GET">
  <input type="search" name="q">
  <button>Search</button>
</form>
```

### **POST**
- Sends data in request body
- Not visible in URL
- No character limit
- Use: login, registration, sensitive data

```html
<form action="/login" method="POST">
  <input type="email" name="email">
  <input type="password" name="password">
  <button>Sign In</button>
</form>
```

## Basic validation

HTML5 allows native validation without JavaScript:

```html
<form>
  <input type="email" required>      <!-- Required -->
  <input type="url" required>        <!-- Must be URL -->
  <input type="number" min="1" max="100">  <!-- Numeric range -->
  <input type="text" pattern="[A-Z]{3}">   <!-- Custom pattern -->
  <button type="submit">Send</button>
</form>
```

## Difference between `<input>` and `<button>`

```html
<!-- Input: only submits data -->
<input type="submit" value="Send">

<!-- Button: more flexible -->
<button type="submit">Send</button>
```

`<button>` is recommended because:
- ✅ Allows HTML content inside
- ✅ Easier to style
- ✅ Better accessibility

---

In upcoming topics you'll learn:
1. **Input types** — Email, password, date, etc.
2. **Validation** — HTML5 validation rules
3. **Advanced elements** — Textarea, select, datalist
4. **Accessibility** — Making forms accessible
5. **Best practices** — Security and UX

# Your First HTML Project

Now that you've learned the fundamentals, it's time to create your first real web page. We'll create a simple but complete website that combines everything we've covered.

## Project Objective

You'll create a **personal website** that includes:
- Correct HTML5 structure
- Multiple semantic sections
- Functional navigation
- Properly formatted content
- Internal and external links

## Project Structure

```
my-website/
  ├── index.html
  ├── about-me.html
  ├── projects.html
  ├── contact.html
  └── css/
      └── styles.css
```

## The index.html file

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Personal Page - John Developer</title>
  <meta name="description" content="Welcome to my personal page. I'm a web developer passionate about technology.">
  <link rel="stylesheet" href="css/styles.css">
</head>
<body>
  <!-- Header and navigation -->
  <header>
    <h1>John Developer</h1>
    <nav>
      <a href="index.html">Home</a>
      <a href="about-me.html">About Me</a>
      <a href="projects.html">Projects</a>
      <a href="contact.html">Contact</a>
    </nav>
  </header>

  <!-- Main content -->
  <main>
    <section id="introduction">
      <h2>Welcome</h2>
      <p>Hello, I'm <strong>John</strong>, a Computer Engineering student passionate about web development.</p>
      <p>On this site you'll find information about me and my projects.</p>
    </section>

    <section id="highlights">
      <h2>Highlights</h2>
      <ul>
        <li>Programming in HTML, CSS and JavaScript</li>
        <li>Web application development</li>
        <li>Responsive design</li>
      </ul>
    </section>

    <section id="knowledge">
      <h2>My Knowledge</h2>
      <table>
        <thead>
          <tr>
            <th>Language</th>
            <th>Level</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>HTML</td>
            <td>Intermediate</td>
          </tr>
          <tr>
            <td>CSS</td>
            <td>Basic</td>
          </tr>
          <tr>
            <td>JavaScript</td>
            <td>Basic</td>
          </tr>
        </tbody>
      </table>
    </section>
  </main>

  <!-- Sidebar (optional) -->
  <aside>
    <h3>Useful Links</h3>
    <ul>
      <li><a href="https://github.com" target="_blank" rel="noopener noreferrer">My GitHub</a></li>
      <li><a href="https://linkedin.com" target="_blank" rel="noopener noreferrer">My LinkedIn</a></li>
      <li><a href="mailto:john@example.com">Email me</a></li>
    </ul>
  </aside>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 John Developer. All rights reserved.</p>
    <p><small>Last updated: June 2025</small></p>
  </footer>
</body>
</html>
```

## Other pages

### about-me.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>About Me - John Developer</title>
  <link rel="stylesheet" href="css/styles.css">
</head>
<body>
  <header>
    <h1>John Developer</h1>
    <nav>
      <a href="index.html">Home</a>
      <a href="about-me.html">About Me</a>
      <a href="projects.html">Projects</a>
      <a href="contact.html">Contact</a>
    </nav>
  </header>

  <main>
    <article>
      <h2>About Me</h2>
      <p>I'm a Computer Engineering student at the University...</p>
      <h3>My Journey</h3>
      <p>I started learning programming 3 years ago...</p>
    </article>
  </main>

  <footer>
    <p>&copy; 2025 John Developer.</p>
  </footer>
</body>
</html>
```

## Steps to create your project

1. **Create a folder** called `my-website`
2. **Copy the code** from `index.html` into a new file
3. **Open the page** in your browser (File → Open)
4. **Create the other pages** (`about-me.html`, `projects.html`, `contact.html`)
5. **Verify that links** work between pages
6. **Validate your HTML** at [validator.w3.org](https://validator.w3.org/)

## Next steps

Once you have the basic HTML working:

1. **Learn CSS** to style your page
2. **Add JavaScript** for interactivity
3. **Publish your site** on GitHub Pages or a web server
4. **Keep improving** your project

## Review Checklist

- [ ] All files are in UTF-8
- [ ] You have a correct DOCTYPE
- [ ] Navigation works between pages
- [ ] External links open in new tab (with `target="_blank"`)
- [ ] Your HTML validates without errors
- [ ] Relative paths work correctly
- [ ] You used semantic tags (`<header>`, `<main>`, `<footer>`, etc.)

Congratulations! You've created your first website. Now it's time to style it and make it more interesting.

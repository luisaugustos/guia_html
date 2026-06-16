# Elementos Semánticos HTML

La **semántica HTML** significa usar etiquetas que describan correctamente el significado de su contenido. No es solo sobre cómo se ve en el navegador, sino sobre qué *significa* ese contenido.

## ¿Por qué importa la semántica?

Usar HTML semántico es importante para:

1. **Motores de búsqueda** — entienden mejor tu contenido para SEO
2. **Lectores de pantalla** — ayuda a personas con discapacidad visual
3. **Mantenibilidad** — tu código es más fácil de entender y modificar
4. **Accesibilidad** — cumples con estándares web importantes

## Ejemplo: Semántico vs. No semántico

**Incorrecto (no semántico):**
```html
<div>
  <div><b>Mi Artículo</b></div>
  <div>Fecha: 15 de junio</div>
  <div>Aquí va el contenido del artículo...</div>
</div>
```

**Correcto (semántico):**
```html
<article>
  <h1>Mi Artículo</h1>
  <time datetime="2025-06-15">15 de junio</time>
  <p>Aquí va el contenido del artículo...</p>
</article>
```

## Etiquetas semánticas principales

### Estructura general
- `<header>` — encabezado de la página o sección
- `<nav>` — menú de navegación
- `<main>` — contenido principal único (solo uno por página)
- `<section>` — sección temática
- `<article>` — contenido independiente (blog post, noticia, etc.)
- `<aside>` — barra lateral o contenido relacionado
- `<footer>` — pie de página

### Texto y contenido
- `<h1>` a `<h6>` — encabezados (h1 es el más importante)
- `<p>` — párrafo
- `<strong>` — texto importante (no es solo negrita)
- `<em>` — énfasis (no es solo cursiva)
- `<mark>` — texto resaltado
- `<small>` — texto pequeño (anotaciones, copyright)
- `<code>` — código de programación
- `<pre>` — texto preformateado

### Listas
- `<ul>` — lista desordenada (bullets)
- `<ol>` — lista ordenada (números)
- `<li>` — elemento de lista
- `<dl>` — lista de definiciones
- `<dt>` — término a definir
- `<dd>` — definición del término

### Citas y referencias
- `<blockquote>` — cita larga
- `<q>` — cita corta inline
- `<cite>` — referencia a una obra
- `<abbr>` — abreviatura

## Estructura de una página HTML semántica

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <title>Mi Blog</title>
</head>
<body>
  <header>
    <h1>Mi Sitio Web</h1>
    <nav>
      <a href="/">Inicio</a>
      <a href="/blog">Blog</a>
      <a href="/contacto">Contacto</a>
    </nav>
  </header>

  <main>
    <article>
      <h2>Mi Primer Artículo</h2>
      <p>Contenido...</p>
    </article>
  </main>

  <aside>
    <h3>Artículos Recientes</h3>
    <ul>
      <li><a href="#">Artículo 1</a></li>
      <li><a href="#">Artículo 2</a></li>
    </ul>
  </aside>

  <footer>
    <p>&copy; 2025 Mi Sitio Web</p>
  </footer>
</body>
</html>
```

## Diferencia entre `<strong>` y `<b>`

- `<strong>` — texto **importante** (semántico)
- `<b>` — texto en **negrita** (solo presentación)

Lo mismo con `<em>` vs `<i>`.

## Accesibilidad y semántica

Cuando usas HTML semántico:

- Los lectores de pantalla entienden la estructura
- Los buscadores indexan mejor tu contenido
- Tu página es más fácil de mantener
- Cumples con estándares WCAG

Próximos capítulos te mostrarán cómo usar cada una de estas etiquetas en detalle.

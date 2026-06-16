# Tu Primer Proyecto HTML

Ahora que has aprendido los conceptos fundamentales, es momento de crear tu primer página web de verdad. Vamos a crear un sitio simple pero completo que combines todo lo que hemos visto.

## Objetivo del proyecto

Crearás una **página web personal** que incluya:
- Estructura HTML5 correcta
- Múltiples secciones semánticas
- Navegación funcional
- Contenido formateado correctamente
- Enlaces internos y externos

## Estructura del proyecto

```
mi-sitio-web/
  ├── index.html
  ├── sobre-mi.html
  ├── proyectos.html
  ├── contacto.html
  └── css/
      └── estilos.css
```

## El archivo index.html

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mi Página Personal - Juan Developer</title>
  <meta name="description" content="Bienvenido a mi página personal. Soy un desarrollador web apasionado por la tecnología.">
  <link rel="stylesheet" href="css/estilos.css">
</head>
<body>
  <!-- Encabezado y navegación -->
  <header>
    <h1>Juan Developer</h1>
    <nav>
      <a href="index.html">Inicio</a>
      <a href="sobre-mi.html">Sobre Mí</a>
      <a href="proyectos.html">Proyectos</a>
      <a href="contacto.html">Contacto</a>
    </nav>
  </header>

  <!-- Contenido principal -->
  <main>
    <section id="presentacion">
      <h2>Bienvenido</h2>
      <p>Hola, soy <strong>Juan</strong>, estudiante de Ingeniería Informática apasionado por el desarrollo web.</p>
      <p>En este sitio encontrarás información sobre mí y mis proyectos.</p>
    </section>

    <section id="destacados">
      <h2>Destacados</h2>
      <ul>
        <li>Programación en HTML, CSS y JavaScript</li>
        <li>Desarrollo de aplicaciones web</li>
        <li>Diseño responsivo</li>
      </ul>
    </section>

    <section id="conocimientos">
      <h2>Mis Conocimientos</h2>
      <table>
        <thead>
          <tr>
            <th>Lenguaje</th>
            <th>Nivel</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>HTML</td>
            <td>Intermedio</td>
          </tr>
          <tr>
            <td>CSS</td>
            <td>Básico</td>
          </tr>
          <tr>
            <td>JavaScript</td>
            <td>Básico</td>
          </tr>
        </tbody>
      </table>
    </section>
  </main>

  <!-- Barra lateral (opcional) -->
  <aside>
    <h3>Enlaces Útiles</h3>
    <ul>
      <li><a href="https://github.com" target="_blank" rel="noopener noreferrer">Mi GitHub</a></li>
      <li><a href="https://linkedin.com" target="_blank" rel="noopener noreferrer">Mi LinkedIn</a></li>
      <li><a href="mailto:juan@ejemplo.com">Enviarme email</a></li>
    </ul>
  </aside>

  <!-- Pie de página -->
  <footer>
    <p>&copy; 2025 Juan Developer. Todos los derechos reservados.</p>
    <p><small>Última actualización: June 2025</small></p>
  </footer>
</body>
</html>
```

## Otras páginas

### sobre-mi.html
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sobre Mí - Juan Developer</title>
  <link rel="stylesheet" href="css/estilos.css">
</head>
<body>
  <header>
    <h1>Juan Developer</h1>
    <nav>
      <a href="index.html">Inicio</a>
      <a href="sobre-mi.html">Sobre Mí</a>
      <a href="proyectos.html">Proyectos</a>
      <a href="contacto.html">Contacto</a>
    </nav>
  </header>

  <main>
    <article>
      <h2>Sobre Mí</h2>
      <p>Soy un estudiante de Ingeniería Informática en la Universidad...</p>
      <h3>Mi Recorrido</h3>
      <p>Comencé a aprender programación hace 3 años...</p>
    </article>
  </main>

  <footer>
    <p>&copy; 2025 Juan Developer.</p>
  </footer>
</body>
</html>
```

## Pasos para crear tu proyecto

1. **Crea una carpeta** llamada `mi-sitio-web`
2. **Copia el código** de `index.html` en un archivo nuevo
3. **Abre la página** en tu navegador (File → Open)
4. **Crea las otras páginas** (`sobre-mi.html`, `proyectos.html`, `contacto.html`)
5. **Verifica que los enlaces** funcionen entre páginas
6. **Valida tu HTML** en [validator.w3.org](https://validator.w3.org/)

## Siguientes pasos

Una vez que tengas el HTML básico funcionando:

1. **Aprende CSS** para estilizar tu página
2. **Añade JavaScript** para interactividad
3. **Publica tu sitio** en GitHub Pages o un servidor web
4. **Sigue mejorando** tu proyecto

## Checklist de revisión

- [ ] Todos los archivos están en UTF-8
- [ ] Tienes un DOCTYPE correcto
- [ ] La navegación funciona entre páginas
- [ ] Los enlaces externos abren en nueva pestaña (con `target="_blank"`)
- [ ] Tu HTML valida sin errores
- [ ] Las rutas relativas funcionan correctamente
- [ ] Usaste etiquetas semánticas (`<header>`, `<main>`, `<footer>`, etc.)

¡Felicidades! Has creado tu primer sitio web. Ahora es momento de estilizarlo y hacerlo más interesante.

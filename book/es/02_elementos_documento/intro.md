# El Documento HTML: Estructura Interna

Cada página HTML tiene una estructura interna específica. Aunque en el navegador solo ves el contenido del `<body>`, hay mucho más que ocurre en la cabeza (`<head>`) del documento.

## Estructura completa de un documento HTML

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Título de mi página</title>
    <link rel="icon" href="favicon.ico">
    <meta name="description" content="Descripción breve">
  </head>
  <body>
    <h1>Contenido visible aquí</h1>
  </body>
</html>
```

## ¿Qué es el `<head>`?

El `<head>` es el **encabezado del documento**. Contiene:

- **Metadatos** — información sobre la página
- **Enlaces** — a hojas de estilos, fuentes, iconos
- **Título** — lo que aparece en la pestaña del navegador
- **Scripts** — código JavaScript
- **Instrucciones** — cómo debe interpretar el navegador el contenido

El contenido del `<head>` **no aparece en la página**, solo el del `<body>`.

## El atributo `lang`

Siempre especifica el idioma principal:

```html
<html lang="es">  <!-- Español -->
<html lang="en">  <!-- Inglés -->
<html lang="fr">  <!-- Francés -->
```

Esto es importante para:
- Motores de búsqueda (SEO)
- Lectores de pantalla (accesibilidad)
- Correctores ortográficos del navegador

## Meta charset

Especifica la **codificación de caracteres** del documento:

```html
<meta charset="UTF-8">
```

UTF-8 es el estándar moderno y soporta todos los idiomas y símbolos. **Siempre usa UTF-8**.

## Meta viewport

Hace que la página sea **responsiva** (se adapte a pantallas móviles):

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Sin esto, tu página se vería mal en móviles.

## El título de la página

```html
<title>Mi Primer Sitio Web</title>
```

El título aparece en:
- La pestaña del navegador
- Los resultados de búsqueda
- El historial del navegador

**Regla importante**: cada página debe tener un título único y descriptivo.

## Favicon

El **favicon** es el pequeño icono que aparece en la pestaña del navegador:

```html
<link rel="icon" href="favicon.ico">
```

Puedes usar:
- `favicon.ico` — formato tradicional
- `favicon.png` — formato moderno
- `favicon.svg` — vectorial (recomendado)

## Meta description

Una breve descripción de tu página que aparece en los resultados de búsqueda:

```html
<meta name="description" content="Aprende HTML desde cero. Una guía práctica para ingenieros informáticos.">
```

Debe tener entre 150-160 caracteres para verse completa en Google.

## Meta tags para redes sociales

Controla cómo aparece tu página al compartirla en redes:

```html
<meta property="og:title" content="Mi Primer Sitio Web">
<meta property="og:description" content="Descripción breve">
<meta property="og:image" content="imagen.png">
<meta property="og:url" content="https://ejemplo.com">
```

Estos son tags **Open Graph** usados por Facebook, Twitter, LinkedIn, etc.

## Vinculación de hojas de estilos

```html
<link rel="stylesheet" href="estilos.css">
```

Por convencion, los enlaces CSS se ponen en el `<head>`.

## Scripts

```html
<script src="script.js"></script>
```

Aunque técnicamente pueden ir en el `<head>` o al final del `<body>`, generalmente se ponen al final del `<body>` para que la página cargue más rápido.

En los siguientes capítulos profundizaremos en cada uno de estos elementos.

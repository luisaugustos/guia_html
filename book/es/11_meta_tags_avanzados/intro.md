# Meta Tags Avanzados (Open Graph, Twitter Cards, PWA)

Los **meta tags avanzados** controlan cómo tus páginas aparecen en **redes sociales**, **motores de búsqueda** y **aplicaciones web progresivas**.

## Open Graph (OG)

Open Graph permite controlar qué **imagen, título y descripción** se muestran cuando compartes tu página en redes sociales.

### Meta tags Open Graph

```html
<head>
  <!-- Título del página (para OG) -->
  <meta property="og:title" content="Guía de HTML para Ingeniería">
  
  <!-- Descripción (para OG) -->
  <meta property="og:description" content="Aprende HTML desde cero con ejemplos prácticos">
  
  <!-- Imagen que se muestra (recomendado 1200x630px) -->
  <meta property="og:image" content="https://ejemplo.com/portada.jpg">
  
  <!-- URL de la página -->
  <meta property="og:url" content="https://ejemplo.com/html">
  
  <!-- Tipo de contenido -->
  <meta property="og:type" content="website">
  
  <!-- Idioma (opcional) -->
  <meta property="og:locale" content="es_ES">
</head>
```

### Ejemplo completo

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Guía de HTML | USAL</title>
  
  <!-- Meta estándar SEO -->
  <meta name="description" content="Tutorial interactivo de HTML para estudiantes de Ingeniería Informática">
  <meta name="keywords" content="HTML5, web development, tutorial">
  
  <!-- Open Graph para redes sociales -->
  <meta property="og:title" content="Guía de HTML para Ingeniería Informática">
  <meta property="og:description" content="Tutorial interactivo de HTML5 para estudiantes de la USAL">
  <meta property="og:image" content="https://guia.ejemplo.com/og-image.jpg">
  <meta property="og:url" content="https://guia.ejemplo.com/html">
  <meta property="og:type" content="website">
  <meta property="og:site_name" content="Guía HTML USAL">
  
  <!-- Twitter Card -->
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:title" content="Guía de HTML para Ingeniería">
  <meta name="twitter:description" content="Aprende HTML desde cero">
  <meta name="twitter:image" content="https://guia.ejemplo.com/twitter-image.jpg">
  <meta name="twitter:site" content="@usal">
</head>
<body>
  <!-- Contenido... -->
</body>
</html>
```

## Twitter Cards

Las **Twitter Cards** controlan cómo tu contenido aparece en Twitter/X cuando alguien lo comparte.

### Tipos de Twitter Cards

#### `summary` — Tarjeta simple

```html
<meta name="twitter:card" content="summary">
<meta name="twitter:title" content="Mi artículo">
<meta name="twitter:description" content="Descripción breve">
<meta name="twitter:image" content="https://ejemplo.com/imagen.jpg">
```

#### `summary_large_image` — Imagen grande

```html
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Mi artículo">
<meta name="twitter:description" content="Descripción breve">
<meta name="twitter:image" content="https://ejemplo.com/imagen-grande.jpg">
```

#### `player` — Para vídeos/audio

```html
<meta name="twitter:card" content="player">
<meta name="twitter:player" content="https://ejemplo.com/player">
<meta name="twitter:player:width" content="550">
<meta name="twitter:player:height" content="310">
```

### Atributos adicionales

```html
<!-- Nombre de usuario de Twitter -->
<meta name="twitter:creator" content="@tu_usuario">
<meta name="twitter:site" content="@nombre_sitio">

<!-- Dimensiones de imagen recomendadas -->
<!-- summary: 200x200px mínimo, 1MB máximo -->
<!-- summary_large_image: 506x506px mínimo, 1MB máximo -->
```

## PWA (Progressive Web App)

Las **PWA** son aplicaciones web que funcionan sin conexión y se pueden instalar en dispositivos.

### Manifest.json

```json
{
  "name": "Guía de HTML",
  "short_name": "HTML Guide",
  "description": "Tutorial interactivo de HTML para ingeniería",
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

### Link a manifest en HTML

```html
<head>
  <link rel="manifest" href="/manifest.json">
  
  <!-- Color de la barra de estado en móvil -->
  <meta name="theme-color" content="#1976d2">
  
  <!-- Icono para Apple -->
  <link rel="apple-touch-icon" href="/icon-180x180.png">
</head>
```

### Service Worker

```html
<!-- Registrar Service Worker -->
<script>
  if ('serviceWorker' in navigator) {
    navigator.serviceWorker.register('/sw.js')
      .then(() => console.log('SW registrado'))
      .catch(err => console.log('Error:', err));
  }
</script>
```

## Meta tags para móvil

```html
<!-- Viewport (esencial para responsive) -->
<meta name="viewport" content="width=device-width, initial-scale=1">

<!-- Permitir instalación en pantalla de inicio -->
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="Guía HTML">

<!-- Color de la barra de direcciones en Android -->
<meta name="theme-color" content="#1976d2">

<!-- Deshabilitar zoom (usar con cuidado) -->
<!-- <meta name="viewport" content="user-scalable=no"> -->
```

## Meta tags SEO completos

```html
<head>
  <!-- Meta básico -->
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  
  <!-- SEO -->
  <title>Guía de HTML | USAL</title>
  <meta name="description" content="Tutorial de HTML para Ingeniería Informática">
  <meta name="keywords" content="HTML, web, tutorial, USAL">
  <meta name="author" content="Luis Augusto Silva">
  
  <!-- Open Graph -->
  <meta property="og:title" content="Guía de HTML">
  <meta property="og:description" content="Tutorial interactivo">
  <meta property="og:image" content="https://ejemplo.com/og.jpg">
  <meta property="og:url" content="https://ejemplo.com">
  <meta property="og:type" content="website">
  
  <!-- Twitter -->
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:title" content="Guía de HTML">
  <meta name="twitter:description" content="Tutorial interactivo">
  <meta name="twitter:image" content="https://ejemplo.com/twitter.jpg">
  
  <!-- PWA -->
  <link rel="manifest" href="/manifest.json">
  <meta name="theme-color" content="#1976d2">
  
  <!-- Favicon -->
  <link rel="icon" href="/favicon.ico">
  <link rel="apple-touch-icon" href="/apple-icon.png">
  
  <!-- Canonical (para duplicados) -->
  <link rel="canonical" href="https://ejemplo.com/html">
</head>
```

## Validar meta tags

**Herramientas útiles:**

- **Open Graph Debugger** — https://developers.facebook.com/tools/debug/
- **Twitter Card Validator** — https://cards-dev.twitter.com/validator
- **Google Search Console** — https://search.google.com/search-console/
- **Lighthouse** (en DevTools) — Auditar PWA

## Checklist meta tags

- ✅ `og:title`, `og:description`, `og:image` para redes sociales
- ✅ Imagen OG: 1200x630px mínimo
- ✅ Twitter Card tipo apropiado (`summary_large_image` recomendado)
- ✅ `manifest.json` para PWA
- ✅ `theme-color` para móvil
- ✅ `viewport` para responsive
- ✅ `canonical` si hay duplicados
- ✅ `description` para SEO
- ✅ Validar con herramientas oficiales

---

Con estos meta tags avanzados, tu página tendrá mejor **visibilidad en redes sociales**, **mejor SEO**, y podrá funcionar como una **aplicación web progresiva**. ¡Felicidades, has completado la guía de HTML!

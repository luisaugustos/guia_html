# Multimedia en HTML

Los elementos multimedia permiten integrar imágenes, audio y video directamente en tus páginas HTML. HTML5 proporciona etiquetas nativas sin necesidad de plugins externos.

## ¿Qué es multimedia?

Multimedia se refiere a:
- 🖼️ **Imágenes** — PNG, JPG, SVG, WebP
- 🔊 **Audio** — MP3, OGG, WAV
- 🎥 **Video** — MP4, WebM, OGG
- 📺 **Contenido incrustado** — iframes, maps

## Imágenes con `<img>`

La etiqueta más básica:

```html
<img src="imagen.jpg" alt="Descripción">
```

**Atributos importantes:**
- `src` — Ruta de la imagen (obligatorio)
- `alt` — Texto alternativo (obligatorio para accesibilidad)
- `width` / `height` — Dimensiones
- `loading="lazy"` — Carga perezosa

### Imágenes responsivas

Para que las imágenes se adapten a diferentes pantallas:

```html
<img 
  src="imagen.jpg" 
  srcset="
    imagen-small.jpg 600w,
    imagen-medium.jpg 1000w,
    imagen-large.jpg 1600w"
  sizes="(max-width: 600px) 100vw, 
         (max-width: 1000px) 75vw, 
         90vw"
  alt="Descripción">
```

- `srcset` — Lista de imágenes según ancho
- `sizes` — Qué imagen usar según viewport
- El navegador elige automáticamente

### Elemento `<picture>` para control total

```html
<picture>
  <source media="(min-width: 1200px)" srcset="imagen-grande.jpg">
  <source media="(min-width: 600px)" srcset="imagen-media.jpg">
  <img src="imagen-pequena.jpg" alt="Descripción">
</picture>
```

Uso: diferentes imágenes según dispositivo o formato.

## Audio con `<audio>`

Reproducción de audio nativa:

```html
<audio controls>
  <source src="cancion.mp3" type="audio/mpeg">
  <source src="cancion.ogg" type="audio/ogg">
  Tu navegador no soporta audio HTML5.
</audio>
```

**Atributos:**
- `controls` — Muestra controles de reproducción
- `autoplay` — Reproduce automáticamente
- `loop` — Repetición continua
- `muted` — Silenciado por defecto
- `preload="auto|metadata|none"` — Cómo cargar

**Formatos:**
- MP3 — Compatible con todos
- OGG — Alternativa libre
- WAV — Alta calidad

## Video con `<video>`

Reproducción de video nativa:

```html
<video controls width="640" height="360">
  <source src="video.mp4" type="video/mp4">
  <source src="video.webm" type="video/webm">
  Tu navegador no soporta video HTML5.
</video>
```

**Atributos:**
- `controls` — Controles de reproducción
- `poster="imagen.jpg"` — Imagen previa
- `autoplay` — Reproduce automáticamente
- `loop` — Repetición
- `muted` — Silenciado
- `preload` — Cómo cargar

**Formatos:**
- MP4 — Mejor compatibilidad
- WebM — Mejor compresión
- OGG — Alternativa libre

## Subtítulos y pistas de texto

```html
<video controls>
  <source src="video.mp4">
  <track kind="subtitles" src="subtitulos-es.vtt" srclang="es" label="Español">
  <track kind="subtitles" src="subtitles-en.vtt" srclang="en" label="English">
  <track kind="captions" src="captions.vtt" srclang="es">
</video>
```

**Tipos de track:**
- `subtitles` — Traducción del diálogo
- `captions` — Transcripción completa (incluyendo sonidos)
- `descriptions` — Descripción para usuarios con discapacidad visual

## iframes para contenido externo

```html
<iframe 
  src="https://www.youtube.com/embed/VIDEO_ID" 
  width="560" 
  height="315" 
  frameborder="0" 
  allowfullscreen>
</iframe>
```

**Atributos de seguridad:**
- `sandbox` — Restricciones de seguridad
- `allow` — Permisos específicos

**Ejemplo seguro:**
```html
<iframe 
  src="https://www.youtube.com/embed/VIDEO_ID"
  sandbox="allow-playback allow-same-origin"
  title="Video de YouTube">
</iframe>
```

## Mejores prácticas multimedia

### ✅ Haz multimedia accesible
```html
<img src="grafico.png" alt="Gráfico de ventas Q1 2026">
<audio controls>
  <source src="podcast.mp3">
  <p>Tu navegador no soporta audio.</p>
</audio>
```

### ✅ Usa formatos múltiples
```html
<video controls>
  <source src="video.mp4" type="video/mp4">
  <source src="video.webm" type="video/webm">
</video>
```

### ✅ Optimiza imágenes
- Usa la herramienta responsiva `srcset`
- Comprime sin perder calidad
- Considera WebP como alternativa moderna

### ✅ Lazy loading
```html
<img src="imagen.jpg" loading="lazy" alt="...">
```

### ❌ Evita
- Audio/video que se reproduce automáticamente sin permiso
- Imágenes sin atributo `alt`
- Contenido multimedia sin alternativas de texto

---

En los próximos temas aprenderás:
1. Imágenes responsivas en detalle
2. Optimización de multimedia
3. Integración con JavaScript
4. Accesibilidad en multimedia

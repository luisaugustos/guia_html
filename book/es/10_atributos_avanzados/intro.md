# Atributos Avanzados (Data Attributes y Globales)

Los **atributos avanzados** permiten almacenar datos personalizados, controlar comportamientos especiales y mejorar la interactividad de tus páginas HTML sin necesidad de JavaScript complejo.

## Atributos de datos (`data-*`)

Los atributos `data-*` permiten **almacenar información personalizada** en elementos HTML, accesibles desde JavaScript:

```html
<!-- Elemento con datos personalizados -->
<div class="producto" 
     data-id="12345" 
     data-precio="29.99" 
     data-disponible="true">
  Laptop Gaming
</div>

<button data-accion="guardar" data-confirmacion="true">
  Guardar cambios
</button>
```

### Acceso desde JavaScript

```javascript
// Obtener datos
const producto = document.querySelector('.producto');
console.log(producto.dataset.id);        // "12345"
console.log(producto.dataset.precio);    // "29.99"
console.log(producto.dataset.disponible); // "true"

// Establecer datos
producto.dataset.estado = 'vendido';
```

### Casos de uso comunes

```html
<!-- E-commerce: información de producto -->
<div class="item-carrito" 
     data-sku="PROD-001" 
     data-cantidad="2" 
     data-total="59.98">
  <h3>Producto A</h3>
  <p>$29.99 x 2</p>
</div>

<!-- Formularios: validación personalizada -->
<input type="text" 
       data-validar="email" 
       data-requerido="true"
       placeholder="Tu email">

<!-- Galerías: información de imagen -->
<img src="foto.jpg" 
     alt="Descripción" 
     data-autor="Juan García"
     data-año="2026"
     data-licencia="CC-BY-4.0">

<!-- Animaciones: configuración -->
<div class="animacion" 
     data-duracion="2000" 
     data-retardo="500"
     data-repetir="infinite">
  Contenido animado
</div>
```

## Atributos globales

Los **atributos globales** funcionan en **cualquier elemento HTML**:

### `id` — Identificador único

```html
<!-- Define un identificador único para el elemento -->
<h1 id="titulo-principal">Bienvenido</h1>

<!-- Usar en enlaces internos -->
<a href="#titulo-principal">Ir al título</a>

<!-- Usar en JavaScript -->
<button onclick="document.getElementById('titulo-principal').style.color='red';">
  Cambiar color
</button>
```

**Reglas:**
- ✅ Identificador único por página
- ✅ Sin espacios ni caracteres especiales
- ✅ Comenzar con letra o guion bajo

### `class` — Clases CSS

```html
<!-- Aplicar múltiples clases -->
<div class="contenedor principal largo">
  Contenido con múltiples estilos
</div>

<!-- CSS -->
<style>
  .contenedor { padding: 20px; }
  .principal { font-weight: bold; }
  .largo { width: 100%; }
</style>
```

### `style` — Estilos inline (no recomendado)

```html
<!-- Estilos directos (evitar cuando sea posible) -->
<p style="color: blue; font-size: 18px;">
  Párrafo con estilos inline
</p>

<!-- ✓ MEJOR: Usar clases en CSS externo -->
<p class="texto-destacado">
  Párrafo con clase
</p>
```

### `title` — Información al pasar el ratón

```html
<!-- Tooltip al pasar el ratón -->
<button title="Haz clic para guardar">Guardar</button>

<img src="foto.jpg" 
     alt="Descripción" 
     title="Foto de la USAL (2026)">

<abbr title="Asamblea General Ordinaria">AGO</abbr>
```

### `hidden` — Ocultar elementos

```html
<!-- Ocultar elemento sin quitarlo del DOM -->
<div hidden>
  Contenido oculto (no se ve pero existe en HTML)
</div>

<!-- Mostrar con JavaScript -->
<button onclick="document.querySelector('div').hidden = false;">
  Mostrar
</button>
```

### `tabindex` — Orden de navegación por teclado

```html
<!-- Elemento enfocable por teclado -->
<div tabindex="0" role="button">Elemento interactivo</div>

<!-- Elementos sin navegación por teclado (ej: decorativos) -->
<span tabindex="-1">Elemento no navegable</span>

<!-- EVITAR: Orden positivo rompe el flujo natural -->
<!-- ✗ MALO: <div tabindex="1">...</div> -->
```

### `contenteditable` — Editar contenido

```html
<!-- Permitir edición de contenido -->
<div contenteditable="true">
  Este texto se puede editar haciendo clic
</div>

<!-- Solo lectura -->
<div contenteditable="false">
  Este texto no se puede editar
</div>
```

### `spellcheck` — Verificación ortográfica

```html
<!-- Activar verificación ortográfica -->
<textarea spellcheck="true" 
          placeholder="Escribe aquí..."></textarea>

<!-- Desactivar verificación -->
<input type="text" spellcheck="false">
```

### `draggable` — Arrastrable

```html
<!-- Hacer elemento arrastra ble -->
<div draggable="true">
  Puedo ser arrastrado
</div>

<img src="imagen.jpg" draggable="true" alt="Imagen arrastra ble">
```

### `lang` — Idioma

```html
<!-- Especificar idioma para accesibilidad y SEO -->
<html lang="es">
  <head>
    <title>Mi página</title>
  </head>
  <body>
    <p>Texto en español</p>
    <p lang="en">Text in English</p>
    <p lang="fr">Texte en français</p>
  </body>
</html>
```

### `dir` — Dirección de texto

```html
<!-- Texto de derecha a izquierda -->
<div dir="rtl">
  النص العربي يكتب من اليمين إلى اليسار
</div>

<!-- Texto de izquierda a derecha (defecto) -->
<div dir="ltr">
  El texto se lee de izquierda a derecha
</div>
```

## Atributos especiales

### `aria-*` — Accesibilidad (ARIA)

```html
<!-- Define el rol del elemento -->
<div role="button" aria-pressed="false">
  Botón simulado
</div>

<!-- Etiqueta para lectores de pantalla -->
<button aria-label="Cerrar menú">×</button>

<!-- Descripción adicional -->
<input aria-describedby="pwd-hint">
<p id="pwd-hint">Mínimo 8 caracteres</p>
```

### `rel` — Relación con recursos externos

```html
<!-- Enlace a hoja de estilos -->
<link rel="stylesheet" href="estilos.css">

<!-- Favicon -->
<link rel="icon" href="favicon.ico">

<!-- Precargar recurso -->
<link rel="preload" href="fuente.woff2" as="font">

<!-- Enlace a versión alternativa -->
<link rel="alternate" href="/en/" hreflang="en">
```

## Checklist atributos avanzados

- ✅ Usar `data-*` para datos personalizados
- ✅ `id` único por página
- ✅ `class` para estilos CSS (no `style` inline)
- ✅ `title` para información adicional
- ✅ `hidden` para ocultar elementos
- ✅ `tabindex="0"` para elementos interactivos
- ✅ `lang` en idiomas múltiples
- ✅ `aria-*` para accesibilidad
- ✅ `rel` para relaciones correctas

---

En el siguiente capítulo aprenderás sobre **Meta Tags** avanzados para SEO, redes sociales y aplicaciones web progresivas.

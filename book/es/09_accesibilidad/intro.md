# Accesibilidad en HTML (WCAG y ARIA)

La **accesibilidad web** significa crear sitios que todos puedan usar, incluyendo personas con discapacidades. Es un derecho, una responsabilidad legal y una buena práctica de ingeniería.

## ¿Por qué es importante la accesibilidad?

1. **Inclusión** — Beneficia a ~15% de la población mundial con discapacidades
2. **Legal** — Muchos países tienen leyes que exigen accesibilidad (ADA en USA, AODA en Canadá)
3. **SEO** — Google premia sitios accesibles
4. **Negocio** — Llega a más usuarios
5. **Calidad** — Código más semántico y mantenible

## Normas WCAG (Web Content Accessibility Guidelines)

Las pautas WCAG 2.1 definen tres niveles:

- **A** — Cumplimiento básico
- **AA** — Cumplimiento intermedio (recomendado)
- **AAA** — Cumplimiento máximo

Principios fundamentales (POUR):

1. **P**ercibible — Información perceptible
2. **O**perable — Navegación por teclado
3. **U**nderstandable — Contenido comprensible
4. **R**obust — Compatible con tecnologías asistivas

## Semántica HTML correcta

El primer paso es usar las **etiquetas HTML correctas**:

```html
<!-- ✓ CORRECTO: Semántico -->
<header>
  <nav>
    <ul>
      <li><a href="/inicio">Inicio</a></li>
      <li><a href="/acerca">Acerca de</a></li>
    </ul>
  </nav>
</header>

<main>
  <article>
    <h1>Título del artículo</h1>
    <p>Contenido...</p>
  </article>
</main>

<footer>
  <p>&copy; 2026</p>
</footer>

<!-- ✗ INCORRECTO: Divs genéricos -->
<div class="header">
  <div class="nav">
    <div class="menu">...</div>
  </div>
</div>
```

**Etiquetas semánticas importantes:**
- `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<aside>`, `<footer>`
- `<h1>` a `<h6>` para encabezados (en orden)
- `<label>` para campos de formulario
- `<table>` para datos tabulares

## Atributos `alt` en imágenes

El atributo `alt` es **obligatorio** y crítico:

```html
<!-- ✓ BUENO: Descripción meaningful -->
<img src="grafico-ventas.png" alt="Gráfico de ventas Q1 2026 mostrando incremento del 15%">

<!-- ✓ ACEPTABLE: Imagen decorativa -->
<img src="linea-separadora.png" alt="">

<!-- ✗ MALO: Sin descripción -->
<img src="grafico.png">

<!-- ✗ MALO: Redundante -->
<img src="foto.jpg" alt="foto"> <!-- "foto" no es útil -->
```

**Regla:** Si la imagen comunica información, describe qué dice. Si es puramente decorativa, usa `alt=""`.

## ARIA (Accessible Rich Internet Applications)

ARIA proporciona **atributos** para describir rol, estado y propiedades de elementos:

### Roles ARIA

```html
<!-- Definir rol de un elemento -->
<div role="button" onclick="hacer_algo()">Clic aquí</div>

<div role="alert">¡Advertencia importante!</div>

<div role="navigation">...</div>

<div role="search">...</div>
```

### Etiquetas y descripciones

```html
<!-- aria-label: etiqueta invisible -->
<button aria-label="Cerrar menú">×</button>

<!-- aria-labelledby: referencia a otro elemento -->
<h2 id="dialogo-titulo">Confirmar acción</h2>
<div role="dialog" aria-labelledby="dialogo-titulo">
  ¿Estás seguro?
</div>

<!-- aria-describedby: descripción adicional -->
<input type="password" aria-describedby="pwd-hint">
<p id="pwd-hint">Mínimo 8 caracteres, incluir números</p>
```

### Propiedades de estado

```html
<!-- aria-expanded: expandido/colapsado -->
<button aria-expanded="false" aria-controls="menu">Menú</button>
<div id="menu" hidden>Opciones...</div>

<!-- aria-current: página actual -->
<nav>
  <a href="/inicio" aria-current="page">Inicio</a>
  <a href="/acerca">Acerca de</a>
</nav>

<!-- aria-disabled: deshabilitado -->
<button aria-disabled="true">No disponible</button>

<!-- aria-live: actualizaciones en vivo -->
<div aria-live="polite" aria-atomic="true">
  Nuevos mensajes cargados...
</div>
```

## Navegación por teclado

### Orden de tabulación

```html
<!-- Usa tabindex=0 para elementos interactivos no estándar -->
<div tabindex="0" role="button">Clickeable</div>

<!-- Evita tabindex positivo (rompe el orden natural) -->
<!-- ✗ MALO: tabindex="1", tabindex="2", etc. -->

<!-- Para remover de la navegación por teclado -->
<div tabindex="-1">No navegable por teclado</div>
```

### Focus visible

```html
<!-- Asegúrate de que el focus sea visible -->
<style>
  button:focus {
    outline: 2px solid blue;
    outline-offset: 2px;
  }
</style>

<!-- ✗ MALO: Remover el outline sin alternativa -->
button:focus {
  outline: none; /* Nunca hagas esto solo */
}
```

## Contraste de colores

WCAG AA requiere:
- **Normal:** ratio 4.5:1
- **Grande:** ratio 3:1

```html
<!-- ✓ BUENO: Contraste suficiente -->
<p style="color: #000; background: #fff;">Texto de alto contraste</p>

<!-- ✗ MALO: Contraste insuficiente -->
<p style="color: #ccc; background: #ddd;">Difícil de leer</p>
```

## Estructura de encabezados

```html
<!-- ✓ CORRECTO: Jerarquía lógica -->
<h1>Título principal de la página</h1>

<section>
  <h2>Sección 1</h2>
  <h3>Subsección 1.1</h3>
  <h3>Subsección 1.2</h3>
</section>

<section>
  <h2>Sección 2</h2>
</section>

<!-- ✗ INCORRECTO: Saltos de nivel -->
<h1>Título</h1>
<h3>Salto directo a h3</h3> <!-- Confuso para lectores de pantalla -->
```

## Lectores de pantalla

Los usuarios ciegos/visuales usan lectores como:
- NVDA (gratuito, Windows)
- JAWS (Windows)
- VoiceOver (macOS/iOS)
- TalkBack (Android)

**Consejo:** prueba tu sitio con NVDA para verificar accesibilidad.

## Checklist de accesibilidad básica

- ✅ Usa etiquetas HTML semánticas
- ✅ Todo contenido visual tiene atributo `alt`
- ✅ Formularios tienen etiquetas `<label>`
- ✅ Contraste de color >= 4.5:1
- ✅ Navegable por teclado (Tab, Enter, Escape)
- ✅ Focus visible en todos los elementos interactivos
- ✅ Encabezados en orden jerárquico
- ✅ Videos tienen subtítulos y descripciones
- ✅ Enlaces tienen texto descriptivo (no "clic aquí")
- ✅ El sitio funciona sin JavaScript

---

En los próximos temas aprenderás:
1. ARIA en profundidad
2. Testing de accesibilidad
3. Herramientas de auditoría
4. Patrones accesibles comunes

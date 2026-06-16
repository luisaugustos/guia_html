# Anatomía Detallada de las Etiquetas

Entender la estructura completa de una etiqueta es fundamental para trabajar correctamente con HTML.

## Partes de una etiqueta

```html
<p class="importante" id="parrafo-1">Esto es contenido</p>
```

1. **Símbolo de apertura** (`<`) — marca el inicio
2. **Nombre de la etiqueta** (`p`) — define qué tipo de elemento es
3. **Atributos** (`class="importante" id="parrafo-1"`) — información adicional
4. **Símbolo de cierre** (`>`) — termina la etiqueta de apertura
5. **Contenido** (`Esto es contenido`) — lo que se muestra o procesa
6. **Etiqueta de cierre** (`</p>`) — marca el final del elemento

## Tipos de etiquetas comunes

### Contenedores
Son etiquetas que contienen otras etiquetas o contenido:

```html
<div>...</div>    <!-- Bloque genérico -->
<section>...</section>  <!-- Sección semántica -->
<article>...</article>  <!-- Artículo -->
<nav>...</nav>    <!-- Navegación -->
<header>...</header>    <!-- Encabezado -->
<footer>...</footer>    <!-- Pie de página -->
<main>...</main>   <!-- Contenido principal -->
```

### De texto
Etiquetas que formatean texto:

```html
<h1>...</h1>  <!-- Encabezado nivel 1 -->
<p>...</p>    <!-- Párrafo -->
<strong>...</strong>  <!-- Texto fuerte (importante) -->
<em>...</em>  <!-- Énfasis -->
<small>...</small>    <!-- Texto pequeño -->
<span>...</span>  <!-- Texto genérico inline -->
```

### Vacías (auto-cerrables)
No contienen contenido ni etiqueta de cierre:

```html
<img src="..." alt="...">
<input type="...">
<br>
<hr>
<meta name="..." content="...">
<link rel="..." href="...">
```

## Jerarquía y anidamiento correcto

Las etiquetas deben anidarse correctamente:

```html
<!-- ✓ CORRECTO: Los elementos se cierran en orden -->
<div>
  <p>
    <strong>Texto importante</strong> en un párrafo
  </p>
</div>

<!-- ✗ INCORRECTO: Solapamiento de etiquetas -->
<div>
  <p>
    <strong>Texto importante</p>
  </strong>
</div>
```

## Atributos comunes en todas las etiquetas

Algunos atributos funcionan en casi cualquier etiqueta:

| Atributo | Descripción | Ejemplo |
|---|---|---|
| `id` | Identificador único del elemento | `id="seccion-1"` |
| `class` | Clase CSS para estilos | `class="destacado"` |
| `style` | Estilos CSS inline | `style="color: red;"` |
| `title` | Texto que aparece al pasar el ratón | `title="Ver más"` |
| `data-*` | Datos personalizados | `data-numero="42"` |

## DOCTYPE y declaración HTML

El **DOCTYPE** no es realmente una etiqueta, pero es obligatorio al inicio del documento:

```html
<!DOCTYPE html>
```

Esto le dice al navegador que use la especificación HTML5. En HTML versiones anteriores había varias variantes, pero en HTML5 solo existe una.

Inmediatamente después viene la etiqueta raíz:

```html
<!DOCTYPE html>
<html lang="es">
  ...
</html>
```

El atributo `lang` especifica el idioma principal del documento (importante para accesibilidad y SEO).

## Validación de HTML

Para verificar que tu HTML es correcto, puedes usar el validador oficial del W3C:

1. Ve a [https://validator.w3.org/](https://validator.w3.org/)
2. Introduce tu código o URL
3. El validador te mostrará errores y advertencias

Mantener HTML válido es importante para:
- Compatibilidad entre navegadores
- Accesibilidad
- SEO (posicionamiento en buscadores)
- Mantenibilidad del código

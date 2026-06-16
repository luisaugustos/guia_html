# Enlaces e Hipervínculos

Los **enlaces** son la esencia de la web. Sin ellos, no habría forma de navegar de una página a otra. En esta sección aprenderás cómo crear y gestionar enlaces correctamente.

## La etiqueta `<a>`

La etiqueta `<a>` (anchor) crea un hipervínculo. Su atributo principal es `href` (Hypertext REFerence):

```html
<a href="https://ejemplo.com">Haz clic aquí</a>
```

El texto entre `<a>` y `</a>` es lo que el usuario ve y puede hacer clic.

## URLs vs. Rutas

Hay dos formas de especificar destinos:

### URLs Absolutas
Dirección web completa:
```html
<a href="https://www.google.com">Google</a>
<a href="http://ejemplo.com/pagina.html">Página externa</a>
```

### Rutas Relativas
Rutas dentro de tu propio sitio:
```html
<a href="pagina.html">Página en el mismo directorio</a>
<a href="carpeta/pagina.html">Página en una carpeta</a>
<a href="../pagina.html">Página en la carpeta padre</a>
<a href="/">Página de inicio</a>
```

## Atributos de enlace

| Atributo | Uso | Ejemplo |
|---|---|---|
| `href` | Destino del enlace | `href="pagina.html"` |
| `target` | Dónde abrir | `target="_blank"` (nueva pestaña) |
| `title` | Texto al pasar el ratón | `title="Ver más información"` |
| `rel` | Relación con el destino | `rel="noopener noreferrer"` |
| `download` | Descargar archivo | `download="archivo.pdf"` |

## Abrir en nueva pestaña

```html
<a href="https://ejemplo.com" target="_blank" rel="noopener noreferrer">
  Abrir en nueva pestaña
</a>
```

El atributo `rel="noopener noreferrer"` es importante por seguridad.

## Enlaces internos dentro de la página

Usa `id` para crear enlaces a secciones:

```html
<!-- Crear un destino -->
<h2 id="seccion-2">Sección 2</h2>

<!-- Crear un enlace a ese destino -->
<a href="#seccion-2">Ir a Sección 2</a>
```

## Descargar archivos

```html
<a href="documento.pdf" download>Descargar PDF</a>
<a href="imagen.png" download="mi-imagen.png">Descargar con nombre diferente</a>
```

## Correo y teléfono

```html
<!-- Enlace de correo -->
<a href="mailto:usuario@ejemplo.com">Enviar correo</a>

<!-- Enlace de teléfono -->
<a href="tel:+34123456789">Llamar</a>

<!-- Correo con parámetros (agrega ?subject=tema al href) -->
<a href="mailto:usuario@ejemplo.com">Enviar consulta</a>
```

## Mejores prácticas

1. **Texto descriptivo** — usa texto que explique adónde lleva el enlace, no "haz clic aquí"
2. **Estructura clara** — los enlaces deben ser fáciles de identificar
3. **Validación de URLs** — verifica que los enlaces funcionen
4. **Accesibilidad** — los enlaces deben ser navegables con teclado

## Diferencia entre rutas

Imagina esta estructura:
```
sitio/
  ├── index.html
  ├── pagina1.html
  └── carpeta/
      └── pagina2.html
```

Desde `carpeta/pagina2.html`:
- `../index.html` → sube una carpeta, accede a index.html
- `../pagina1.html` → sube una carpeta, accede a pagina1.html
- `./archivo.html` → en la carpeta actual
- `../../archivo.html` → sube dos carpetas

En los siguientes capítulos aprenderás más sobre rutas y cómo organizarlas correctamente.

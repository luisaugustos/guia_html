# Conceptos Fundamentales de HTML

En esta sección aprenderás los conceptos básicos que necesitas entender para trabajar con HTML. No es complicado, pero es importante asimilar bien estas ideas desde el principio.

## ¿Qué es una etiqueta (tag)?

Una **etiqueta** es la unidad básica de HTML. Es un código que le dice al navegador cómo debe presentar o interpretar el contenido.

Una etiqueta típica tiene esta estructura:

```html
<nombredelatiqueta>contenido</nombredelatiqueta>
```

Ejemplo:
```html
<p>Este es un párrafo.</p>
```

Aquí, `<p>` es la **etiqueta de apertura**, `Este es un párrafo.` es el **contenido**, y `</p>` es la **etiqueta de cierre**. El navegador interpreta esto como un párrafo.

## Etiquetas de auto-cierre

Algunas etiquetas no tienen contenido y se cierran a sí mismas. Se llaman **etiquetas vacías** o **auto-cerrables**:

```html
<img src="imagen.png" alt="Descripción">
<br>
<input type="text">
```

Estas etiquetas no necesitan una etiqueta de cierre separada.

## ¿Qué son los atributos?

Los **atributos** son propiedades adicionales que añaden información a una etiqueta. Se colocan dentro de la etiqueta de apertura.

```html
<img src="imagen.png" alt="Descripción de la imagen">
```

En este ejemplo:
- `src` es el atributo que especifica la **ruta** de la imagen
- `alt` es el atributo que proporciona **texto alternativo** si la imagen no se puede cargar

Los atributos siempre tienen la forma `nombre="valor"`.

## Anidamiento

Las etiquetas pueden contener otras etiquetas. Esto se llama **anidamiento**. Ejemplo:

```html
<div>
  <h1>Título Principal</h1>
  <p>Este párrafo está dentro del div.</p>
</div>
```

Aquí, `<h1>` y `<p>` están **anidados** dentro del `<div>`. El orden es importante: la etiqueta que se abre primero debe cerrarse al final.

## Estructura básica de un documento HTML

Cada página HTML tiene una estructura mínima:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Título de la página</title>
  </head>
  <body>
    <h1>Contenido aquí</h1>
  </body>
</html>
```

- `<!DOCTYPE html>` — le dice al navegador que es un documento HTML5
- `<html>` — la etiqueta raíz que contiene todo
- `<head>` — contiene información sobre la página (no se ve en el navegador)
- `<body>` — contiene el contenido visible de la página

## Comentarios

Los **comentarios** son anotaciones en el código que el navegador ignora. Son útiles para documentar tu trabajo:

```html
<!-- Esto es un comentario -->
<p>Este texto sí se ve</p>
<!-- Puedes explicar aquí qué hace esta sección -->
```

Los comentarios no aparecen en la página, solo en el código fuente.

## Caracteres especiales

A veces necesitas mostrar caracteres especiales en HTML. Usa **entidades HTML**:

| Carácter | Código | Uso |
|---|---|---|
| `<` | `&lt;` | Menor que |
| `>` | `&gt;` | Mayor que |
| `&` | `&amp;` | Ampersand |
| `"` | `&quot;` | Comillas dobles |
| `'` | `&#39;` | Comillas simples |
| `©` | `&copy;` | Símbolo de copyright |
| `€` | `&euro;` | Símbolo de euro |

Ejemplo:
```html
<p>El precio es &lt; 10€ y la fórmula es E &gt; mc²</p>
```

Próximos capítulos cubrirán cada uno de estos conceptos en profundidad.

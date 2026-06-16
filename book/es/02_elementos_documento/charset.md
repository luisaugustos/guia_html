# Charset (Juego de Caracteres)

El atributo `charset` define qué **juego de caracteres** (encoding) usa el documento HTML. Es fundamental para que los navegadores interpreten correctamente textos en diferentes idiomas y caracteres especiales.

## ¿Qué es charset?

El charset especifica la **codificación de caracteres** que usa el archivo:

- **UTF-8** — Juego universal (recomendado, incluye todos los idiomas)
- **ISO-8859-1** — Caracteres latinos
- **Windows-1252** — Caracteres Windows
- **ASCII** — Caracteres básicos en inglés

## Declarar charset en `<head>`

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Mi Página</title>
</head>
<body>
  <h1>¡Hola, mundo!</h1>
</body>
</html>
```

**Regla importante:** El `<meta charset>` debe ser el **primer elemento** dentro de `<head>` para que el navegador lo procese inmediatamente.

```html
<!-- ✓ CORRECTO: Meta charset es el primero -->
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Página</title>
</head>

<!-- ✗ INCORRECTO: Meta charset no es el primero -->
<head>
  <title>Página</title>
  <meta charset="UTF-8">
</head>
```

## UTF-8: El estándar universal

**UTF-8** es el charset por defecto y recomendado:

✅ Soporta **todos los idiomas** del mundo
✅ Compatible con **caracteres especiales**
✅ Eficiente en **tamaño de archivo**
✅ Estándar web moderno

### Ejemplos de caracteres Unicode soportados

```html
<meta charset="UTF-8">

<!-- Español -->
<p>Acentos: á, é, í, ó, ú, ñ</p>

<!-- Francés -->
<p>Caracteres: ç, è, ê, ë</p>

<!-- Alemán -->
<p>Umlauts: ä, ö, ü, ß</p>

<!-- Caracteres matemáticos y símbolos -->
<p>Símbolos: © ® ™ € ¥ ± × ÷ ≠ ≤ ≥</p>

<!-- Emoji (también UTF-8) -->
<p>Emojis: 🚀 🎉 ❤️ 🌍</p>
```

## Problemas comunes sin charset correcto

Sin declarar `charset="UTF-8"`, el navegador puede mal-interpretar caracteres:

```html
<!-- ✗ MALO: Sin meta charset, caracteres acentuados pueden verse así:
    â€œHolaâ€? en lugar de "Hola"
-->
<head>
  <title>Página sin charset</title>
</head>

<!-- ✓ BUENO: Con charset, todo se ve correcto -->
<head>
  <meta charset="UTF-8">
  <title>Página correcta</title>
</head>
```

## Entidades HTML para caracteres especiales

Si por alguna razón necesitas caracteres especiales sin UTF-8, usa **entidades HTML**:

| Carácter | Entidad | Descripción |
|---|---|---|
| `©` | `&copy;` | Copyright |
| `®` | `&reg;` | Marca registrada |
| `™` | `&trade;` | Marca comercial |
| `€` | `&euro;` | Euro |
| `¥` | `&yen;` | Yen |
| `£` | `&pound;` | Libra |
| `§` | `&sect;` | Sección |
| `¶` | `&para;` | Párrafo |
| `†` | `&dagger;` | Puñal |
| `‡` | `&Dagger;` | Doble puñal |

**Ejemplo:**

```html
<p>Derechos de autor &copy; 2026 Universidad de Salamanca</p>
<!-- Se mostrará como: Derechos de autor © 2026 Universidad de Salamanca -->
```

## Guardar archivos en UTF-8

Asegúrate de que tu **editor de texto** guarde los archivos en **UTF-8**:

### VS Code
1. Haz clic en `UTF-8` en la esquina inferior derecha
2. Selecciona `Save with Encoding...` → `UTF-8`

### Otros editores
- **Notepad++** — Encoding → Encode in UTF-8
- **Sublime Text** — File → Save with Encoding → UTF-8
- **Atom** — File → Save As → Encoding: UTF-8

## Checklist charset

- ✅ `<meta charset="UTF-8">` es el primer elemento en `<head>`
- ✅ Archivo guardado como **UTF-8** en tu editor
- ✅ Caracteres acentuados se ven correctamente en el navegador
- ✅ Emojis y símbolos especiales funcionan
- ✅ No usar charset obsoletos (ISO-8859-1, Windows-1252)

---

Con charset bien configurado, tu página mostrará correctamente cualquier idioma y carácter especial. En el siguiente tema aprenderás sobre otros atributos meta importantes.

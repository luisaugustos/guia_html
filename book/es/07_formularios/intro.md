# Formularios en HTML

Los **formularios** son uno de los elementos más importantes de HTML. Permiten a los usuarios interactuar con tu sitio web, enviando datos al servidor. Todo, desde login hasta búsquedas, pasa por formularios.

## ¿Por qué son importantes los formularios?

Los formularios son la forma principal de:
- ✅ Recolectar información del usuario
- ✅ Procesar datos (login, registro, búsqueda)
- ✅ Permitir interacción bidireccional
- ✅ Mejorar la experiencia del usuario
- ✅ Validar datos antes de enviar al servidor

## Estructura básica de un formulario

Un formulario simple tiene esta estructura:

```html
<form action="/procesar" method="POST">
  <label for="nombre">Nombre:</label>
  <input type="text" id="nombre" name="nombre" required>
  
  <button type="submit">Enviar</button>
</form>
```

## Componentes principales

Un formulario completo incluye:

### 1. **La etiqueta `<form>`**
```html
<form action="/procesar" method="POST">
  <!-- Contenido del formulario -->
</form>
```
- `action` — URL donde se envían los datos
- `method` — Método HTTP: `GET` o `POST`

### 2. **Campos de entrada**
```html
<input type="text" name="usuario">
<textarea name="mensaje"></textarea>
<select name="pais">
  <option>España</option>
</select>
```

### 3. **Etiquetas `<label>`**
```html
<label for="email">Email:</label>
<input type="email" id="email" name="email">
```
- Hacen el formulario accesible
- Aumentan el área clickeable
- Describen el campo

### 4. **Botones**
```html
<button type="submit">Enviar</button>
<button type="reset">Limpiar</button>
<button type="button">Acción</button>
```

## Atributos importantes de `<form>`

| Atributo | Uso | Ejemplo |
|----------|-----|---------|
| `action` | URL destino | `action="/login"` |
| `method` | GET o POST | `method="POST"` |
| `enctype` | Codificación (para archivos) | `enctype="multipart/form-data"` |
| `name` | Nombre del formulario | `name="login-form"` |
| `autocomplete` | Autocompletado | `autocomplete="on"` |
| `novalidate` | Sin validación HTML5 | `novalidate` |

## GET vs POST

### **GET**
- Envía datos en la URL
- Visible en la barra de direcciones
- Limitado a ~2000 caracteres
- Uso: búsquedas, filtros

```html
<form action="/buscar" method="GET">
  <input type="search" name="q">
  <button>Buscar</button>
</form>
```

### **POST**
- Envía datos en el cuerpo de la petición
- No visible en la URL
- Sin límite de caracteres
- Uso: login, registro, datos sensibles

```html
<form action="/login" method="POST">
  <input type="email" name="email">
  <input type="password" name="password">
  <button>Entrar</button>
</form>
```

## Validación básica

HTML5 permite validación nativa sin JavaScript:

```html
<form>
  <input type="email" required>      <!-- Obligatorio -->
  <input type="url" required>        <!-- Debe ser URL -->
  <input type="number" min="1" max="100">  <!-- Rango numérico -->
  <input type="text" pattern="[A-Z]{3}">   <!-- Patrón personalizado -->
  <button type="submit">Enviar</button>
</form>
```

## Diferencia entre `<input>` y `<button>`

```html
<!-- Input: solo envía datos -->
<input type="submit" value="Enviar">

<!-- Button: más flexible -->
<button type="submit">Enviar</button>
```

`<button>` es más recomendado porque:
- ✅ Permite contenido HTML dentro
- ✅ Más fácil de estilizar
- ✅ Mejor accesibilidad

---

En los próximos temas aprenderás:
1. **Tipos de input** — Email, contraseña, fecha, etc.
2. **Validación** — Reglas de validación HTML5
3. **Elementos avanzados** — Textarea, select, datalist
4. **Accesibilidad** — Hacer formularios accesibles
5. **Mejores prácticas** — Seguridad y UX

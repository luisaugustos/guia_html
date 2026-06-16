# Tipos de Input en HTML5

HTML5 proporciona muchos tipos de `<input>` especializados que ofrecen validación automática y mejor experiencia de usuario. Cada tipo tiene un propósito específico.

## Tipos de entrada más comunes

### **1. Text (Texto simple)**
```html
<input type="text" name="nombre" placeholder="Tu nombre">
```
- Texto simple de una línea
- Uso: nombres, direcciones, etc.

### **2. Email**
```html
<input type="email" name="email" required>
```
- Valida formato de email automáticamente
- En móviles muestra teclado email (@)
- Uso: registros, login

### **3. Password (Contraseña)**
```html
<input type="password" name="pass" required>
```
- Oculta el texto mientras se escribe
- Los navegadores pueden guardar/recuperar
- Uso: login, registro

### **4. Number (Número)**
```html
<input type="number" name="edad" min="18" max="120">
```
- Solo números
- Validación de rango (min/max)
- En móviles muestra teclado numérico
- Atributos: `min`, `max`, `step`

### **5. Tel (Teléfono)**
```html
<input type="tel" name="telefono" pattern="[0-9]{9}">
```
- En móviles muestra teclado de teléfono
- No valida formato automáticamente
- Uso: números de teléfono

### **6. URL**
```html
<input type="url" name="sitio" required>
```
- Valida que sea una URL válida
- Uso: sitios web, enlaces

### **7. Date (Fecha)**
```html
<input type="date" name="nacimiento">
```
- Selector de fecha integrado
- En navegadores modernos abre un datepicker
- Formato: YYYY-MM-DD
- Atributos: `min`, `max`

### **8. Time (Hora)**
```html
<input type="time" name="hora">
```
- Selector de hora
- Formato: HH:MM
- Uso: horarios, reservas

### **9. Search (Búsqueda)**
```html
<input type="search" name="q" placeholder="Buscar...">
```
- Optimizado para búsquedas
- En algunos navegadores muestra botón X para limpiar
- Uso: barras de búsqueda

### **10. Range (Rango)**
```html
<input type="range" name="volumen" min="0" max="100" value="50">
```
- Control deslizante
- Valor entre min y max
- Uso: volumen, brillo, zoom

### **11. Checkbox (Casilla)**
```html
<label>
  <input type="checkbox" name="aceptar" value="si">
  Acepto los términos
</label>
```
- Selecciona/deselecciona
- Puede estar marcado o no
- Atributo: `checked`

### **12. Radio (Opción única)**
```html
<label>
  <input type="radio" name="genero" value="masculino"> Masculino
</label>
<label>
  <input type="radio" name="genero" value="femenino"> Femenino
</label>
```
- Solo una opción puede estar seleccionada
- Mismo `name` agrupa las opciones
- Uso: elegir una entre varias

### **13. File (Archivo)**
```html
<input type="file" name="documento" accept=".pdf,.doc">
```
- Abre explorador de archivos
- Atributo `accept` filtra extensiones
- Para múltiples: `multiple`

### **14. Color (Color)**
```html
<input type="color" name="color" value="#FF0000">
```
- Selector de color
- Retorna valor hexadecimal
- Uso: temas personalizados

### **15. Hidden (Oculto)**
```html
<input type="hidden" name="token" value="abc123">
```
- No se muestra al usuario
- Se envía con el formulario
- Uso: tokens, IDs internos

## Tabla de referencia rápida

| Tipo | Validación | Teclado Móvil | Uso |
|------|-----------|--------------|-----|
| text | No | Texto | General |
| email | Sí | Email (@) | Emails |
| password | No | Texto | Contraseñas |
| number | Sí | Numérico | Números |
| tel | No | Teléfono | Teléfonos |
| url | Sí | URL (.) | URLs |
| date | Sí | Datepicker | Fechas |
| time | No | Hora | Horas |
| search | No | Búsqueda | Búsquedas |
| range | No | Deslizador | Rangos |
| checkbox | No | - | Múltiples |
| radio | No | - | Una opción |
| file | No | - | Archivos |
| color | No | - | Colores |
| hidden | No | - | Datos ocultos |

## Atributos comunes para inputs

```html
<input 
  type="text"
  name="usuario"           <!-- Nombre del campo -->
  id="username"            <!-- ID único -->
  value="juan"             <!-- Valor inicial -->
  placeholder="Tu nombre"  <!-- Sugerencia -->
  required                 <!-- Obligatorio -->
  disabled                 <!-- Deshabilitado -->
  readonly                 <!-- Solo lectura -->
  autocomplete="on"        <!-- Autocompletado -->
  maxlength="50"           <!-- Máximo de caracteres -->
  minlength="3"            <!-- Mínimo de caracteres -->
>
```

## Mejor práctica: Sempre usar `<label>`

```html
<!-- ✓ CORRECTO -->
<label for="email">Email:</label>
<input type="email" id="email" name="email">

<!-- ✗ INCORRECTO -->
Email: <input type="email" name="email">
```

Las etiquetas:
- ✅ Hacen el formulario accesible
- ✅ Aumentan el área clickeable
- ✅ Mejoran la experiencia de usuario

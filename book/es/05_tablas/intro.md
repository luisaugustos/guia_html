# Tablas en HTML

Las **tablas** son elementos fundamentales para presentar datos tabulares de forma estructurada. Aunque históricamente se usaron para hacer layouts (hoy usamos CSS para eso), las tablas siguen siendo esenciales para datos reales.

## La estructura básica de una tabla

```html
<table>
  <tr>
    <td>Celda 1</td>
    <td>Celda 2</td>
  </tr>
  <tr>
    <td>Celda 3</td>
    <td>Celda 4</td>
  </tr>
</table>
```

## Etiquetas de tabla

| Etiqueta | Significado | Uso |
|---|---|---|
| `<table>` | Define la tabla | Contenedor principal |
| `<tr>` | Table Row (fila) | Cada fila de datos |
| `<td>` | Table Data (celda) | Datos normales |
| `<th>` | Table Header (encabezado) | Celdas de encabezado |
| `<thead>` | Table Head | Agrupa encabezados |
| `<tbody>` | Table Body | Agrupa cuerpo de datos |
| `<tfoot>` | Table Footer | Agrupa pie de tabla |
| `<caption>` | Caption | Título de la tabla |
| `<colgroup>` | Column Group | Agrupa columnas |
| `<col>` | Column | Define una columna |

## Tabla con estructura completa

```html
<table>
  <caption>Temperaturas Mensuales 2025</caption>
  <thead>
    <tr>
      <th>Mes</th>
      <th>Mínima (°C)</th>
      <th>Máxima (°C)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Enero</td>
      <td>5</td>
      <td>15</td>
    </tr>
    <tr>
      <td>Febrero</td>
      <td>6</td>
      <td>16</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Promedio</td>
      <td>5.5</td>
      <td>15.5</td>
    </tr>
  </tfoot>
</table>
```

## Atributos de celda

| Atributo | Uso | Ejemplo |
|---|---|---|
| `colspan` | Fusionar columnas | `<td colspan="2">` |
| `rowspan` | Fusionar filas | `<td rowspan="3">` |
| `headers` | Asociar a encabezados | `<td headers="col1 col2">` |
| `scope` | Alcance del encabezado | `<th scope="col">` |

## Celdas fusionadas (merged cells)

```html
<table>
  <tr>
    <th>Nombre</th>
    <th colspan="2">Calificaciones</th>
  </tr>
  <tr>
    <td>Juan</td>
    <td>8.5</td>
    <td>9.0</td>
  </tr>
</table>
```

## Accesibilidad en tablas

Para hacer tablas accesibles para lectores de pantalla:

```html
<table>
  <thead>
    <tr>
      <th scope="col" id="mes">Mes</th>
      <th scope="col" id="temp">Temperatura</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td headers="mes">Enero</td>
      <td headers="temp">15°C</td>
    </tr>
  </tbody>
</table>
```

## Tablas complejas

Las tablas complejas con múltiples niveles de encabezados pueden ser difíciles de hacer accesibles. En esos casos, considera:

1. **Simplificar la tabla** si es posible
2. **Dividirla en tablas más simples**
3. **Usar atributos de accesibilidad** como `scope` y `headers`
4. **Proporcionar alternativas** (texto descriptivo, lista, etc.)

## ¿Cuándo usar tablas?

**Úsalas para:**
- Datos tabulares reales
- Comparativas
- Estadísticas
- Horarios

**NO las uses para:**
- Layouts de página (usa CSS Grid o Flexbox)
- Contenido que no es tabular
- Efectos visuales

En próximos capítulos aprenderás a estilizar tablas con CSS para hacerlas más visuales.

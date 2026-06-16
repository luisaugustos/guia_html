# Tables in HTML

**Tables** are fundamental elements for presenting tabular data in a structured way. Although they were historically used for page layouts (we use CSS for that today), tables remain essential for real data.

## Basic table structure

```html
<table>
  <tr>
    <td>Cell 1</td>
    <td>Cell 2</td>
  </tr>
  <tr>
    <td>Cell 3</td>
    <td>Cell 4</td>
  </tr>
</table>
```

## Table tags

| Tag | Meaning | Use |
|---|---|---|
| `<table>` | Defines the table | Main container |
| `<tr>` | Table Row | Each row of data |
| `<td>` | Table Data | Normal cells |
| `<th>` | Table Header | Header cells |
| `<thead>` | Table Head | Groups headers |
| `<tbody>` | Table Body | Groups data body |
| `<tfoot>` | Table Footer | Groups table footer |
| `<caption>` | Caption | Table title |
| `<colgroup>` | Column Group | Groups columns |
| `<col>` | Column | Defines a column |

## Table with complete structure

```html
<table>
  <caption>Monthly Temperatures 2025</caption>
  <thead>
    <tr>
      <th>Month</th>
      <th>Min (°C)</th>
      <th>Max (°C)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>January</td>
      <td>5</td>
      <td>15</td>
    </tr>
    <tr>
      <td>February</td>
      <td>6</td>
      <td>16</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Average</td>
      <td>5.5</td>
      <td>15.5</td>
    </tr>
  </tfoot>
</table>
```

## Cell attributes

| Attribute | Use | Example |
|---|---|---|
| `colspan` | Merge columns | `<td colspan="2">` |
| `rowspan` | Merge rows | `<td rowspan="3">` |
| `headers` | Associate to headers | `<td headers="col1 col2">` |
| `scope` | Header scope | `<th scope="col">` |

## Merged cells

```html
<table>
  <tr>
    <th>Name</th>
    <th colspan="2">Grades</th>
  </tr>
  <tr>
    <td>John</td>
    <td>8.5</td>
    <td>9.0</td>
  </tr>
</table>
```

## Accessibility in tables

To make tables accessible for screen readers:

```html
<table>
  <thead>
    <tr>
      <th scope="col" id="month">Month</th>
      <th scope="col" id="temp">Temperature</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td headers="month">January</td>
      <td headers="temp">15°C</td>
    </tr>
  </tbody>
</table>
```

## Complex tables

Complex tables with multiple levels of headers can be hard to make accessible. In those cases, consider:

1. **Simplify the table** if possible
2. **Split it into simpler tables**
3. **Use accessibility attributes** like `scope` and `headers`
4. **Provide alternatives** (descriptive text, list, etc.)

## When to use tables?

**Use them for:**
- Real tabular data
- Comparisons
- Statistics
- Schedules

**DON'T use them for:**
- Page layouts (use CSS Grid or Flexbox)
- Non-tabular content
- Visual effects

In upcoming chapters you'll learn to style tables with CSS to make them more visually appealing.

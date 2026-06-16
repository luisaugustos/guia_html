# Guía de HTML para Ingeniería Informática 🌐

[![Licencia: CC BY 4.0](https://img.shields.io/badge/Licencia-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Universidad de Salamanca](https://img.shields.io/badge/USAL-Universidad%20de%20Salamanca-red.svg)](https://www.usal.es)

Libro educativo interactivo de **HTML (HyperText Markup Language)** diseñado para la asignatura **Sistemas y Aplicaciones Informáticas** de **Ingeniería Informática** en la Universidad de Salamanca.

Este material proporciona una introducción pragmática y centrada en competencias a los conceptos fundamentales de HTML que todo ingeniero informático debe dominar, desde la anatomía de las etiquetas hasta la creación de sitios web completos.

---

## 📖 Sobre este libro

**Asignatura**: Sistemas y Aplicaciones Informáticas  
**Grado**: Ingeniería Informática  
**Universidad**: Universidad de Salamanca  
**Guía docente**: https://guias.usal.es/node/199094

Este libro forma parte del material educativo para la asignatura de formación básica en tecnologías de la información y sistemas web.

## 👤 Autor

**Luis Blázquez Medina**  
Departamento de Informática y Automática  
Universidad de Salamanca

- **Perfil de investigador**: https://produccioncientifica.usal.es/investigadores/1285047/detalle
- **GitHub**: [talkdoluis](https://github.com/talkdoluis)
- **Email**: talkdoluis@gmail.com

## 📝 Cita

La cita recomendada está en formato APA 7.ª edición:

> Blázquez Medina, L. (2026). *Guía de HTML para Ingeniería Informática*. Universidad de Salamanca.

Los metadatos reutilizables están en [`CITATION.cff`](CITATION.cff), [`CITATION.bib`](CITATION.bib) y [`.zenodo.json`](.zenodo.json).

---

## 🖥️ Cómo acceder al libro

Este libro está disponible en dos formatos:

| Formato | Acceso | Descripción |
|---|---|---|
| **Web interactiva** | [Online](https://guiadehtml.usal.es) | Versión navegable en navegador (recomendado) |
| **PDF imprimible** | [Descargar PDF](book/_static/GuiaDeHTMLParaIngenieriaInformatica.pdf) | Versión en PDF para imprimir |
| **Repositorio** | [GitHub](https://github.com/talkdoluis/guia-html-usal) | Código fuente y archivos editables |

> **Recomendación**: Usa la versión web para aprender (con búsqueda, ejemplos interactivos). Descarga el PDF si necesitas una versión impresa.

---

## 📋 Requisitos para estudiantes

Para seguir este curso y completar los ejercicios prácticos, necesitas:

### Imprescindible
1. **Editor de código** (elige uno):
   - [VS Code](https://code.visualstudio.com/) ⭐ **Recomendado** (gratuito)
   - [Sublime Text](https://www.sublimetext.com/)
   - [Atom](https://atom.io/)
   - Incluso el Bloc de notas funciona, pero un editor dedicado es mejor

2. **Navegador web moderno**:
   - Chrome, Firefox, Safari o Edge
   - Necesitarás las herramientas de desarrollador (F12)

### Opcional (para ejecutar ejemplos locales)
3. **Python 3.12** → [Descargar](https://www.python.org/downloads/) (si quieres compilar la web localmente)
4. **Git** → [Descargar](https://git-scm.com/) (si quieres clonar el repositorio)

---

## 🎓 Cómo usar este libro

### 📖 Estructura del contenido

El libro está organizado en 6 capítulos progresivos:

1. **Conceptos Fundamentales** — Anatomía de las etiquetas, atributos, anidamiento
2. **El Documento HTML** — Estructura de la página, head, meta tags, favicon, SEO
3. **Elementos Semánticos** — Headers, párrafos, listas, citas, estructura correcta
4. **Enlaces e Hipervínculos** — Rutas, URLs, enlaces internos y externos
5. **Tablas** — Estructura de tablas, merged cells, accesibilidad
6. **Tu Primer Proyecto** — Proyecto práctico: crear tu propio sitio web

### 🎯 Recomendaciones de aprendizaje

- **Lee en orden** — cada capítulo se construye sobre los anteriores
- **Experimenta** — copia los ejemplos en tu editor y modifica el código
- **Practica** — completa los ejercicios al final de cada capítulo
- **Usa las herramientas** — abre el inspector de elementos (F12) para ver cómo funciona
- **Consulta el código** — estudia sitios web reales para entender patrones

### 💡 Consejos prácticos

1. Escribe el código tú mismo, no lo copies y pegues
2. Valida tu HTML en [validator.w3.org](https://validator.w3.org/)
3. Usa el inspector de elementos del navegador (F12) para aprender
4. Lee la documentación oficial: [MDN Web Docs](https://developer.mozilla.org/es/docs/Learn/HTML)

---

## 📂 Estructura del proyecto

```
guia-html-usal/
├── book/                          # Contenido del libro
│   ├── es/                        # Capítulos en español
│   │   ├── intro.md               # Introducción al libro
│   │   ├── 01_conceptos_fundamentales/
│   │   ├── 02_elementos_documento/
│   │   ├── 03_elementos_semanticos/
│   │   ├── 04_enlaces/
│   │   ├── 05_tablas/
│   │   └── 06_primer_html/
│   ├── en/                        # Capítulos en inglés (misma estructura)
│   ├── _static/                   # Imágenes, CSS, logos
│   ├── _config_es.yml             # Configuración español
│   ├── _toc_es.yml                # Índice español
│   ├── _config_en.yml             # Configuración inglés
│   └── _toc_en.yml                # Índice inglés
├── scripts/                       # Scripts de compilación (uso interno)
├── HTML/                          # Archivos HTML de referencia originales
├── AGENTS.md                      # Documentación técnica del proyecto
└── README.md                      # Este archivo
```

### 📝 Recursos para estudiantes

- Los ejemplos de código están en los capítulos
- Los ejercicios prácticos al final de cada capítulo
- Enlaces a recursos externos como [MDN Web Docs](https://developer.mozilla.org/)

---

## 🌍 Disponible en varios idiomas

Este libro está disponible en:

- **Español (es)** — Idioma principal, versión completa
- **English (en)** — Versión en inglés, contenido equivalente

En la web, encontrarás un selector de idioma en la esquina superior para cambiar entre versiones. El contenido es equivalente en ambas versiones.

---

## 📚 Bibliografía y referencias

La forma más simple de gestionar bibliografía en esta plantilla es:

1. guardar todas las entradas BibTeX en:
   - `book/_static/references.bib`
2. citar en cualquier página con:
   - `{cite:t}`
   - `{cite:p}`
3. usar la página final de:
   - `Referencias` / `References`

Esa página imprime la bibliografía global del libro y sirve también para la exportación a PDF/LaTeX.

---

## ❓ Preguntas frecuentes

**P: ¿Puedo descargar el libro en PDF?**  
R: Sí, descargalo desde la sección "Cómo acceder al libro" arriba. También está disponible en la web con un botón de descarga.

**P: ¿Puedo usar este material en mi propio curso?**  
R: Sí, está licenciado bajo CC BY 4.0. Puedes reutilizarlo siempre que atribuas la autoría.

**P: ¿Hay ejercicios prácticos?**  
R: Sí, cada capítulo incluye ejercicios y un proyecto final para aplicar lo aprendido.

**P: ¿Dónde reporto problemas o sugerencias?**  
R: Contacta con el autor o abre un issue en el repositorio de GitHub.

---

## 🔧 Para desarrolladores / Contribuyentes

Si deseas contribuir mejoras a este libro:

1. **Fork** el repositorio
2. Crea una **rama** con tus cambios
3. Haz **commit** con mensajes descriptivos
4. Abre un **Pull Request**

El libro se compila automáticamente en GitHub Pages con cada actualización.

### Tecnología utilizada

- **Jupyter Book** — Framework para libros interactivos
- **MyST Markdown** — Markdown con capacidades extendidas
- **Sphinx** — Generador de documentación
- **Python 3.12** — Lenguaje base de los scripts
- **TeachBook** — Plantilla educativa

---

## 📄 Licencia

Este proyecto está licenciado bajo **CC BY 4.0** — eres libre de usar, modificar y redistribuir con atribución.

---

## 🙏 Agradecimientos y Referencias

Este libro se construyó usando:

- [**Jupyter Book**](https://jupyterbook.org/) — Framework para libros técnicos interactivos
- [**TeachBook**](https://teachbooks.io/) — Plantilla educativa para profesores
- [**MyST Markdown**](https://myst-parser.readthedocs.io/) — Markdown científico
- [**MDN Web Docs**](https://developer.mozilla.org/) — Referencia de HTML

**Inspirado en**:
- La guía del curso "Elaboración de libros electrónicos mediante código y asistentes de IA" (Lozano Murciego & Sales Mendes)
- Material educativo de la Universidad de Salamanca
- Mejores prácticas de enseñanza de tecnologías web

---

**¿Preguntas o sugerencias?**  
Contacta con: **talkdoluis@gmail.com**  
O abre un issue en el repositorio de GitHub.

---
{"dg-publish":true,"permalink":"/Notas/Apuntes/Estructura de página html moderna/"}
---


## 🧱 ¿Cómo se estructura el `<body>` de una página HTML moderna?

Una estructura semántica y correcta podría verse así:

```html
<body>
  <header>
    <nav>
      <ul>
        <li><a href="#">Inicio</a></li>
        <li><a href="#">Contacto</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section>
      <h2>Bienvenido</h2>
      <p>Contenido de bienvenida.</p>
    </section>

    <section>
      <h2>Últimas noticias</h2>
      <article>...</article>
      <article>...</article>
    </section>
  </main>

  <aside>
    <h2>Publicidad</h2>
    <p>Contenido adicional.</p>
  </aside>

  <footer>
    <p>&copy; 2025 Francisco Rey</p>
  </footer>
</body>

```

### 🧩 Tabla de Etiquetas Semánticas HTML5

| **Etiqueta**    | **Función / Definición Semántica**                                                                    | **Uso Común / Buenas Prácticas**                                                |
| --------------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `<header>`      | Encabezado de una página o sección. Contiene introducción, títulos, logotipos o navegación.           | Usar 1 global dentro de `<body>` y también local en `<article>` o `<section>`.  |
| `<main>`        | Contenido principal y único de la página, excluye encabezado, pie, navegación o contenido secundario. | Solo uno por página. No debe estar dentro de `<header>`, `<footer>`, etc.       |
| `<footer>`      | Pie de página o sección. Contiene información legal, enlaces secundarios, créditos, contacto.         | Puede usarse global o dentro de un `<section>` o `<article>`.                   |
| `<nav>`         | Bloque de navegación principal o secundaria. Contiene enlaces a otras partes del sitio.               | No para cualquier `<ul>`, solo si representa navegación significativa.          |
| `<section>`     | Bloque temático del documento. Puede tener su propio `<h2>`, `<h3>`, etc.                             | Ideal para dividir contenido en temas claros con título.                        |
| `<article>`     | Contenido autónomo y reutilizable, como entradas de blog, noticias o comentarios.                     | Contiene título, texto y puede tener su propio `<header>` y `<footer>`.         |
| `<aside>`       | Contenido relacionado o adicional, como barras laterales, anuncios, widgets o notas.                  | Usar para info que complementa pero no interrumpe el flujo principal.           |
| `<h1>` a `<h6>` | Encabezados jerárquicos. Describen niveles de contenido.                                              | Usar de forma estructurada. Un `<h1>` por página suele ser buena práctica.      |
| `<address>`     | Información de contacto del autor o entidad responsable del contenido.                                | Se puede incluir dentro de `<footer>`. No usar para cualquier dirección postal. |
| `<figure>`      | Contenedor de contenido ilustrativo (imagen, gráfico, código, etc.)                                   | Se usa junto a `<figcaption>`. Ayuda a describir medios insertados.             |
| `<figcaption>`  | Pie de figura para describir el contenido de un `<figure>`.                                           | Debe ir como hijo directo de `<figure>`.                                        |
| `<mark>`        | Marca texto relevante o destacado en el contexto actual.                                              | Para resaltar términos en una búsqueda o advertencia.                           |
| `<time>`        | Representa una hora o fecha específica en formato legible o ISO.                                      | Útil para eventos, publicaciones, calendarios.                                  |
| `<summary>`     | Título visible del contenido plegable dentro de un `<details>`.                                       | Mejora la accesibilidad de bloques colapsables.                                 |
| `<details>`     | Contenido colapsable (plegable), que el usuario puede expandir o contraer.                            | Muy útil para FAQ, políticas, filtros, etc.                                     |

### 📝 Notas clave:

- Todas estas etiquetas tienen significado **semántico**, es decir, **comunican estructura y propósito** a navegadores, motores de búsqueda y lectores de pantalla.
- Su uso **mejora el SEO, la accesibilidad** y el mantenimiento del código.
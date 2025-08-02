---
{"dg-publish":true,"permalink":"/Notas/Apuntes/CSS Grid/"}
---


# CSS Grid
CSS Grid es otro sistema de diseño que permite organizar elementos en una cuadrícula bidimensional. Puedes definir filas, columnas, áreas y espacios entre ellos. Aquí tienes un ejemplo básico:

```css
/* Contenedor de rejilla */
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: auto;
}

/* Elementos de la rejilla */
.item {
  grid-column: 2 / 3;
  grid-row: 1;
}
```

CSS Grid fuerza de alguna manera a tener un pensamiento visual mas cercano al diseño de grilla trdicional de prensa, que define previamente un lienzo bidimensional del cual se ajustan los elementos de manera más libre.

### Cuándo usar CSS Grid

- Para realizar plantillas o layouts más complejos que los que harías con [[Notas/Apuntes/Flexbox\|Flexbox]].
- Para diseños que escapan del sistema tradicional de secciones apiladas verticalmente con filas de cajas.
- Para hacer patrones de visualización complejos como [[Notas/Apuntes/Masonry Layout (UI)\|Masonry Layout (UI)]].
# Reto 01 - Fijando la barra de navegación a la parte superior de la pantalla

## Introducción

En este reto trabajaremos con uno de los elementos más importantes de cualquier sitio web: la barra de navegación. Vamos a asegurarnos de que esta se mantenga visible en la parte superior de la pantalla incluso cuando el usuario haga scroll. Esto es una práctica común en diseño web moderno y mejora considerablemente la experiencia de navegación.

---

## Objetivos

- Aplicar posicionamiento fijo a la barra de navegación.
- Utilizar clases utilitarias de Bootstrap para lograr este efecto.
- Ajustar los estilos para que el contenido visual se mantenga limpio y legible.

---

## Requisitos

- Tener Visual Studio Code instalado (u otro editor de código).
- Haber creado previamente tu archivo `index.html` con la barra de navegación.
- Tener cargado Bootstrap en tu proyecto.
- Comprender el concepto de diseño responsive.

---

## Desarrollo paso a paso

### Paso 1: Analizar el comportamiento actual

Abre tu archivo `index.html` y visualiza la página en el navegador. Observa que al hacer scroll, la barra de navegación desaparece. El objetivo es fijarla en la parte superior de la pantalla.

### Paso 2: Agregar la clase `fixed-top`

Bootstrap ofrece una clase utilitaria llamada `fixed-top` que hace exactamente lo que necesitamos. Agrégala directamente en el elemento `<nav>` de tu barra de navegación:

```html
<nav class="navbar navbar-expand-lg navbar-light fixed-top">
  <!-- Contenido de la barra de navegación -->
</nav>
```

Guarda los cambios y actualiza tu navegador. Verás que la barra ahora se queda fija mientras haces scroll.

### Paso 3: Asegurar visibilidad con fondo

Es posible que al hacer scroll, el contenido pase por detrás de la barra de navegación, dificultando la lectura. Para evitarlo, asegurémonos de que la barra tenga un color de fondo definido. Esto se puede hacer desde tu archivo CSS, agregando el siguiente bloque:

```css
.navbar {
  background-color: #fffbf7;
  text-align: center;
  color: #025157;
  font-weight: 500;
}
```

Esto garantiza que el texto sea visible y que la barra tenga contraste con el resto del contenido.

---

## Resultado esperado

Una barra de navegación que permanece fija en la parte superior al hacer scroll, con estilos claros y legibles. La experiencia de usuario mejora porque los visitantes siempre tienen acceso al menú de navegación.

---


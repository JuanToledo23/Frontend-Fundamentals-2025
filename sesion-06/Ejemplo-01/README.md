# 🧪 Ejemplo 01 – Agregando JavaScript de Bootstrap al Proyecto

## 🧠 Introducción

¡Bienvenido al primer ejemplo de la sesión!  
Antes de empezar a usar componentes modernos como **carruseles**, **menús colapsables** o **acordeones**, necesitamos asegurarnos de que **Bootstrap 5** esté bien integrado en nuestro proyecto.

Recuerda que Bootstrap funciona con dos piezas clave:

1. **CSS**: Para los estilos, el diseño, las clases visuales como botones, márgenes, contenedores, etc.
2. **JavaScript (JS)**: Para que los componentes interactivos funcionen correctamente (por ejemplo, el botón de menú hamburguesa en móvil, los sliders, etc.).

En este ejemplo, vas a integrar ambas cosas desde un CDN (Content Delivery Network), lo que significa que no necesitas descargar archivos, solo enlazarlos.

Vamos a usar todo esto dentro de tu página **"Descubre México"**, así que asegúrate de tener abierto tu archivo `index.html`.

---

## 🎯 Objetivos

Al terminar este ejercicio podrás:

- Conectar correctamente Bootstrap 5 a tu proyecto web.
- Habilitar los estilos prediseñados de Bootstrap.
- Activar los componentes interactivos que requieren JavaScript.
- Dejar tu página lista para usar componentes modernos y reutilizables.

---

## ✅ Requisitos

Asegúrate de tener lo siguiente antes de comenzar:

- Visual Studio Code instalado.
- Tu proyecto “Descubre México” con el archivo `index.html` ya creado.
- Conexión a internet (ya que usaremos los archivos desde la nube, vía CDN).

---

## 🛠 Desarrollo paso a paso

### 🔹 Paso 1: Agrega el archivo CSS de Bootstrap

Bootstrap tiene un archivo CSS que contiene todas las clases visuales que usaremos (como `.btn`, `.card`, `.navbar`, etc.).

1. Abre tu archivo `index.html`.
2. Dentro de la etiqueta `<head>`, **antes de tu archivo `styles.css`**, pega este código:

```html
<!-- Bootstrap 5 CSS -->
<link
  href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
  rel="stylesheet"
/>
```

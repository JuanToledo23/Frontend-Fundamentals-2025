# 🧪 Ejemplo 02 – Agregando un Carrusel con Bootstrap

## 🧠 Introducción

Un carrusel (o carousel) es un componente visual que permite mostrar imágenes o contenido destacado de forma rotativa. Es perfecto para darle dinamismo a la portada de un sitio web y captar la atención del usuario desde el primer momento.

En este ejemplo reemplazaremos el banner estático de la landing page **“Descubre México”** por un carrusel de Bootstrap completamente funcional. Usaremos imágenes icónicas de México y aprenderemos cómo personalizar el contenido y los controles de este componente.

---

## 🎯 Objetivos

- Reemplazar el banner original por un carrusel funcional.
- Comprender la estructura de un carrusel en Bootstrap 5.
- Insertar imágenes relevantes con texto superpuesto.
- Asegurar que el componente sea 100% responsivo.

---

## ✅ Requisitos

- Bootstrap 5 ya integrado en el archivo `index.html`.
- Tener acceso al archivo `index.html` del proyecto **“Descubre México”**.
- Visual Studio Code y navegador abiertos para ver los cambios.

---

## 🛠 Desarrollo paso a paso

### Paso 1: Comentar el banner original

En `index.html`, comenta la sección del banner para que no se muestre pero se conserve:

```html
<!--
<section class="banner">
  <h1>Descubre la Belleza de México</h1>
  <p>Un país lleno de historia, cultura y paisajes impresionantes.</p>
</section>
-->
```

---

### Paso 2: Insertar el carrusel

Justo después de tu barra de navegación (`</nav>`), agrega el siguiente bloque de código:

```html
<div id="carouselMexico" class="carousel slide mt-5" data-bs-ride="carousel">
  <!-- Indicadores -->
  <div class="carousel-indicators">
    <button
      type="button"
      data-bs-target="#carouselMexico"
      data-bs-slide-to="0"
      class="active"
      aria-current="true"
      aria-label="Slide 1"
    ></button>
    <button
      type="button"
      data-bs-target="#carouselMexico"
      data-bs-slide-to="1"
      aria-label="Slide 2"
    ></button>
    <button
      type="button"
      data-bs-target="#carouselMexico"
      data-bs-slide-to="2"
      aria-label="Slide 3"
    ></button>
  </div>

  <!-- Contenido del carrusel -->
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src="./img/mexico.jpg" class="d-block w-100" alt="México" />
      <div class="carousel-caption d-none d-md-block">
        <h5>Descubre la Belleza de México</h5>
        <p>Un país lleno de historia, cultura y paisajes impresionantes.</p>
      </div>
    </div>
    <div class="carousel-item">
      <img
        src="./img/chichenitza.jpeg"
        class="d-block w-100"
        alt="Chichén Itzá"
      />
    </div>
    <div class="carousel-item">
      <img src="./img/cancun.jpg" class="d-block w-100" alt="Cancún" />
    </div>
  </div>

  <!-- Controles de navegación -->
  <button
    class="carousel-control-prev"
    type="button"
    data-bs-target="#carouselMexico"
    data-bs-slide="prev"
  >
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Anterior</span>
  </button>
  <button
    class="carousel-control-next"
    type="button"
    data-bs-target="#carouselMexico"
    data-bs-slide="next"
  >
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Siguiente</span>
  </button>
</div>
```

---

## 🔍 ¿Cómo funciona este carrusel?

- **`.carousel-inner`** contiene los slides.
- Cada **`.carousel-item`** es una imagen o contenido a mostrar.
- Solo uno debe tener la clase `active` para que se muestre primero.
- **`.carousel-caption`** te permite colocar texto sobre la imagen.
- Las flechas (`prev` y `next`) permiten avanzar o retroceder manualmente.
- Los botones circulares de **`.carousel-indicators`** te muestran en qué slide estás.

---

### Paso 3: ¿Quieres una versión más limpia?

Si no quieres mostrar las flechas de navegación, simplemente elimina estas líneas:

```html
<button class="carousel-control-prev" ...></button>
<button class="carousel-control-next" ...></button>
```

---

## ✅ Resultado esperado

Tu sitio ahora debería mostrar un carrusel moderno con tres imágenes rotando automáticamente.  
También verás:

- Indicadores activos que te permiten saltar de slide.
- Texto superpuesto en la primera imagen.
- Comportamiento responsivo en todas las pantallas.

---

## 💡 Extra

Puedes agregar más slides, tarjetas, videos o incluso formularios dentro del carrusel. Cada `carousel-item` puede contener cualquier estructura HTML, no solo imágenes.

---

## ⏭️ ¿Qué sigue?

Vamos a agregar una **tarjeta personalizada** dentro del carrusel para combinar imágenes con contenido enriquecido.

➡️ [Siguiente reto: Agregar el carrusel y la primer tarjeta](../reto-02/README.md)

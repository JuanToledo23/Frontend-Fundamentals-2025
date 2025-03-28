# 🧪 Ejemplo 03: Agregando segunda columna del blog

---

## 🎯 Objetivos

- Utilizar componentes visuales de Bootstrap para construir una tarjeta de blog.
- Completar la segunda columna de la sección Blog en la landing _Descubre México_.
- Integrar estilos personalizados con Sass sobre un componente de Bootstrap.

---

## ✅ Requisitos previos

- Tener instalado **Visual Studio Code**.
- Conocer los estilos base y clases de **Bootstrap 5**.
- Haber completado el Ejemplo 02 con la primera columna del blog.
- Tener configurado **Sass** y el archivo `main.scss`.

---

## 🧱 Estructura del HTML

Vamos a utilizar el componente [`card`](https://getbootstrap.com/docs/5.3/components/card/) de Bootstrap para crear una entrada de blog. A continuación te muestro el HTML modificado para incluir la **segunda columna** del blog:

```html
<section class="container blog">
  <div class="row">
    <div class="col">
      <!-- Aquí va la columna de descripción (Ejemplo 02) -->
    </div>

    <div class="col">
      <div class="card">
        <img
          src="https://getmatcha.com/wp-content/uploads/2019/03/david-marcu-114194-1052x699.jpg"
          class="card-img-top"
          alt="Ecommerce Blogging: The 2020 Guide for Online Stores and DTC Brands"
        />
        <div class="card-body">
          <h5 class="card-title">
            Ecommerce Blogging: The 2020 Guide for Online Stores and DTC Brands
          </h5>
          <p class="metadata">
            <strong class="category">Performance Blogging</strong>
            <strong class="read-time">• 21 mins read</strong>
          </p>
          <p class="card-text">
            Table of ContentsWhy Ecommerce Businesses Need a Blog in
            2020Document Your Ecommerce Blog StrategyPublication: How to Create
            High-Performing Blog ContentDistribution:...
            <span class="read-more">+ <a href="#">Read More</a></span>
          </p>
          <div class="author">
            <img
              src="https://secure.gravatar.com/avatar/b1c37d9c6b3a36a5eb64d7112bf71ca4?s=96&d=retro&r=g"
              alt="Shauna Ward"
            />
            <p>Shauna Ward</p>
          </div>
        </div>
      </div>
    </div>

    <div class="col">
      <!-- Columna vacía para completar las 3 columnas -->
    </div>
  </div>
</section>
```

---

## 🎨 Estilos personalizados con Sass

Ahora que ya tienes la tarjeta en HTML, es momento de personalizarla con Sass para que se integre visualmente al resto del sitio.

Agrega los siguientes estilos al final de tu archivo `scss/main.scss`:

```scss
.blog {
  .card {
    background-color: $white;
    border: none;
    border-radius: 10px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    margin-top: 20px;

    .card-title {
      font-size: 1.2rem;
      font-weight: bold;
      color: $dark-green-title;
    }

    .metadata {
      font-size: 0.9rem;
      color: $dark-green-text;
      margin: 10px 0;

      .category {
        text-transform: uppercase;
      }

      .read-time {
        margin-left: 8px;
      }
    }

    .card-text {
      font-size: 0.95rem;
      color: $dark-green-text;

      .read-more a {
        color: #007bff;
        text-decoration: none;
        font-weight: bold;
      }

      .read-more a:hover {
        text-decoration: underline;
      }
    }

    .author {
      display: flex;
      align-items: center;
      gap: 10px;
      margin-top: 20px;

      img {
        width: 40px;
        height: 40px;
        border-radius: 50%;
      }

      p {
        margin: 0;
        font-size: 0.9rem;
        color: $dark-green-text;
      }
    }
  }
}
```

> ✅ Este bloque de estilos reutiliza tus variables de color (`$white`, `$dark-green-title`, `$dark-green-text`) definidas en `_global.scss`.

---

## 🧩 Resultado

Al terminar este ejemplo deberías ver una **tarjeta moderna y limpia** en la segunda columna del blog, integrada visualmente al resto del sitio gracias a Bootstrap y Sass.

Puedes seguir usando el patrón de `col` para agregar más columnas o ajustar el diseño para pantallas pequeñas con clases como `col-md`, `col-lg`, etc.

---

📎 [Ir al Reto 01 → Agrega colores usados en las tarjetas](../reto-01/README.md)

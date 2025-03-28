# 🧪 Ejemplo 02: Agregando primera columna del blog

---

## 🎯 Objetivos

- Agregar una nueva hoja de estilos al proyecto.
- Definir **variables** y **placeholders** en Sass/SCSS.
- Utilizar **módulos** (`@use`) para dividir el código en archivos reutilizables.
- Estilizar la primera columna del blog en la landing _Descubre México_ usando Sass.

---

## ✅ Requisitos previos

- Tener instalado **Visual Studio Code**.
- Tener instalado **Dart Sass** o utilizar la extensión **Live Sass Compiler** en VS Code.

---

## 🧱 Estructura del HTML

Agrega esta sección dentro del `<body>` de tu archivo `index.html` justo donde quieras colocar el blog (por ejemplo, antes del `<footer>`):

```html
<section class="container blog">
  <div class="row">
    <div class="col">
      <h2 class="title">Learn how to grow your ecommerce business.</h2>
      <article class="process-list">
        <div class="process">
          <div class="process-icon">
            <img src="./icons/build.svg" alt="Build icon" />
          </div>
          <div class="process-description">
            <h3>Build</h3>
            <p>and scale your ecommerce store</p>
          </div>
        </div>
        <div class="process">
          <div class="process-icon">
            <img src="./icons/attract.svg" alt="Attract icon" />
          </div>
          <div class="process-description">
            <h3>Attract</h3>
            <p>your target audience and grow site traffic</p>
          </div>
        </div>
        <div class="process">
          <div class="process-icon">
            <img src="./icons/convert.svg" alt="Convert icon" />
          </div>
          <div class="process-description">
            <h3>Convert</h3>
            <p>readers to subscribers and customers</p>
          </div>
        </div>
      </article>
      <button>Read the blog</button>
    </div>
    <div class="col"></div>
    <div class="col"></div>
  </div>
</section>
```

> 💡 Los íconos deben guardarse en una carpeta `icons` en la raíz del proyecto.  
> Si no los tienes, puedes usar estos:
>
> - [Build icon](https://cdn.iconscout.com/icon/free/png-256/build-20-454867.png)
> - [Attract icon](https://catwatchful.com/main/wp-content/uploads/2014/09/rocket-icon.png)
> - [Convert icon](https://icon-library.com/images/icon-convert/icon-convert-2.jpg)

---

## 🗂️ Estructura de archivos SCSS

```text
.
├── scss/
│   ├── _global.scss
│   └── main.scss
├── index.html
├── output.css
```

---

## 🎨 Definiendo variables y placeholders

### `scss/_global.scss`

```scss
// Colores
$dark-green-title: #025157;
$dark-green-text: #135359;
$white: #ffffff;

// Tipografías
$font-title: "Alegreya", serif;

// Placeholder reutilizable
%base-title {
  font-family: $font-title;
  color: $dark-green-text;
}
```

---

## 📦 Importando variables con `@use`

### `scss/main.scss`

```scss
@use "global" as *;

.blog {
  background-color: $white;
  max-width: unset;
  padding: 5% 10%;

  .title {
    @extend %base-title;
  }

  .process-list {
    margin-top: 40px;
    margin-bottom: 36px;

    .process {
      margin-bottom: 25px;

      & > div {
        & > h3 {
          color: $dark-green-title;
          margin-bottom: 0;
          font-size: 30px;
          font-weight: 500;
        }

        & > p {
          color: $dark-green-text;
          margin: 0;
        }
      }

      .process-icon {
        width: 60px;
        height: 60px;
        margin-right: 10px;
        text-align: center;

        img {
          height: 100%;
        }
      }
    }
  }

  button {
    height: auto;
    border-top-left-radius: 8px;
    border-bottom-left-radius: 8px;
    padding: 12px;
    width: 180px;
    margin-bottom: 15px;
  }
}
```

---

## ✅ Recuerda:

- `@extend` te permite **heredar estilos comunes**.
- El `parent selector (&)` permite escribir selectores más específicos de forma más limpia.
- `@use` carga módulos SCSS de forma organizada y escalable.

---

¡Listo! Con esto ya tienes completamente estilizada la **primera columna del blog** en tu landing page _Descubre México_ utilizando Sass de forma profesional.

---

📎 [Ir al Ejemplo 03 → Agregando la segunda columna del blog](../Ejemplo-03/README.md)

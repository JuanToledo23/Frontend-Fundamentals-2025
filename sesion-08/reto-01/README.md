# 🧠 Reto 01: Agrega los elementos a la nueva página

---

## 🎯 Objetivos

1. Practicar la maquetación completa de una nueva página en tu sitio **"Descubre México"**.
2. Usar la consola del navegador para inspeccionar elementos, colores y estilos.
3. Preparar la base para agregar transiciones y animaciones en los siguientes retos.

---

## ✅ Requisitos

- Tener instalado **Visual Studio Code**.
- Haber creado la página `about.html` y el archivo `about.scss` en tu proyecto.

---

## 🛠 Instrucciones

En este reto crearás una nueva página que amplíe la información sobre México, aplicando todo lo aprendido hasta ahora en HTML, SCSS, Bootstrap y estructura responsive.

Puedes basarte visualmente en una sección de testimonios, características del país o datos culturales.

---

## ✏️ Paso a paso

### 1. Estructura básica de `about.html`

Usa Emmet para generar la estructura base:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sobre México</title>
  <link rel="stylesheet" href="./about.css" />
</head>
<body>
</body>
</html>
```

> 💡 Pro-tip: Escribe `!` + `Tab` en un archivo `.html` vacío para autocompletar la estructura.

---

### 2. Agrega cabecera y navegación

Copia la cabecera que usas en `index.html` para mantener consistencia. Asegúrate de actualizar los enlaces y el título.

```html
<header>
  <nav>
    <ul>
      <li><a href="./index.html">Inicio</a></li>
      <li><a href="#lugares">Lugares Icónicos</a></li>
      <li><a href="#cultura">Cultura y Tradiciones</a></li>
      <li><a href="./about.html">Sobre México</a></li>
    </ul>
  </nav>
  <div class="actions">
    <a>Sign In</a>
  </div>
</header>
```

---

### 3. Estructura del contenido

Crea una nueva sección principal para mostrar información sobre el país. Puedes usar un diseño de columnas con Bootstrap o Flexbox. Aquí un ejemplo básico con clases personalizadas:

```html
<main class="about-page">
  <section class="top-info">
    <h1>Descubre más sobre México</h1>
    <p>México es un país lleno de contrastes, historia, sabores y colores.</p>
  </section>

  <section class="features">
    <div class="feature">
      <img src="./img/food.svg" alt="Gastronomía">
      <h3>Gastronomía</h3>
      <p>Una de las más reconocidas del mundo por su diversidad de ingredientes, colores y sabores.</p>
    </div>
    <div class="feature">
      <img src="./img/see.png" alt="Naturaleza">
      <h3>Naturaleza</h3>
      <p>Desde playas paradisíacas hasta selvas y montañas, México lo tiene todo.</p>
    </div>
    <div class="feature">
      <img src="./img/chichenitza.jpeg" alt="Historia">
      <h3>Historia</h3>
      <p>Hogar de civilizaciones como los mayas y aztecas, con sitios arqueológicos impresionantes.</p>
    </div>
  </section>
</main>
```

---

### 4. Estilos base en `about.scss`

```scss
.about-page {
  margin-top: 100px;
  padding: 40px 20px;
  text-align: center;

  .top-info {
    margin-bottom: 50px;

    h1 {
      color: #c1272d;
      font-size: 36px;
      font-family: 'Alegreya', serif;
    }

    p {
      font-size: 18px;
      color: #333;
    }
  }

  .features {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    gap: 30px;

    .feature {
      background-color: white;
      border-radius: 10px;
      padding: 20px;
      max-width: 300px;
      box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);

      img {
        width: 100%;
        border-radius: 8px;
        margin-bottom: 15px;
      }

      h3 {
        color: #025157;
        margin-bottom: 10px;
      }

      p {
        font-size: 14px;
        color: #3f3f3f;
      }
    }
  }
}
```

---

### 5. Compila Sass

Ejecuta Sass para que tu archivo `.scss` se convierta en CSS usable por el navegador:

```bash
sass --watch scss/about.scss about.css
```

---

## ✅ Resultado esperado

Tu nueva página `about.html` debe contener una cabecera funcional, una introducción breve y tres tarjetas visuales con contenido informativo sobre México.

📸 Referencia visual:
![Página de About Us completa.](../assets/AboutUsCompleta.png)

---

📎 [Ir al Ejemplo 02 → Transiciones y pseudo-elementos](../Ejemplo-02/README.md)
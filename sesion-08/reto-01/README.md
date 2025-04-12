# 🧠 Reto 01: Agrega los elementos a la nueva página

---

## 🎯 Objetivos

1. Practicar la **maquetación completa** de una nueva página en tu sitio **"Descubre México"**.
2. Usar la consola del navegador para inspeccionar elementos, colores y estilos.
3. Preparar la base visual para aplicar **transiciones y animaciones** en los siguientes ejercicios.

---

## ✅ Requisitos

- Tener instalado **Visual Studio Code**.
- Haber creado los archivos:
  - `about.html` (dentro del proyecto)
  - `_about.scss` (dentro de la carpeta `scss`)
- Tener configurado Sass o Live Sass Compiler.

---

## 🛠 Instrucciones paso a paso

### 1. Crea la estructura base en `about.html`

Abre tu archivo `about.html` y pega el siguiente contenido:

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

  <footer>
    <p>&copy; 2025 Descubre México</p>
  </footer>
</body>
</html>
```

> 💡 Este contenido incluye una cabecera, sección principal con información cultural y una galería de tarjetas.

---

### 2. Crea los estilos en `_about.scss`

Agrega lo siguiente en el archivo `scss/_about.scss`:

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

### 3. Importa `_about.scss` desde `main.scss`

Abre tu archivo `main.scss` y asegúrate de importar la hoja de estilos nueva:

```scss
@use 'about' as *;
```

---

### 4. Compila Sass

En la terminal, asegúrate de estar en la raíz del proyecto y ejecuta:

```bash
sass --watch scss/main.scss about.css
```

> Esto generará un nuevo archivo `about.css` listo para ser usado en el HTML.

---

## ✅ Resultado esperado

Tu nueva página `about.html` debe mostrar lo siguiente:

- ✅ Una cabecera igual a la de `index.html`.
- ✅ Una sección principal con título, párrafo y 3 tarjetas con información cultural.
- ✅ Estilos aplicados desde `about.scss`.

📸 Resultado visual:
![Página de About Us completa.](../assets/AboutUsCompleta.png)

---

## 📚 ¿Qué aprendiste?

- Cómo maquetar una nueva página sin romper el estilo general del sitio.
- Cómo estructurar una sección informativa con tarjetas.
- Cómo preparar la base visual para comenzar a aplicar **animaciones y transiciones** en los siguientes retos.

---

📎 [Ir al Ejemplo 02 → Transiciones y pseudo-elementos](../Ejemplo-02/README.md)
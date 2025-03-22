# Ejercicio 03 - Agregar una nueva página: Gastronomía

## Introducción

Hasta ahora solo hemos trabajado con la página principal del sitio **"Descubre México"**, que muestra lugares icónicos y tradiciones culturales. En este ejercicio aprenderás a **crear una nueva página HTML** que amplíe la experiencia del sitio con más contenido, en este caso, sobre la **Gastronomía Mexicana**. También aprenderás cómo enlazar esta nueva página desde la navegación principal y mantener una apariencia consistente reutilizando estilos.

---

## Objetivos

- Crear una nueva página HTML llamada `gastronomia.html`.
- Enlazarla desde el menú de navegación de `index.html`.
- Reutilizar la estructura y estilos existentes para mantener consistencia.
- Crear contenido sencillo en la nueva página que enriquezca el tema del sitio.

---

## Requisitos

- Tener Visual Studio Code (u otro editor de texto).
- Haber creado previamente el archivo `index.html` y su carpeta `css/` con el archivo `styles.css`.

---

## Paso 1: Crear la nueva página

Dentro de la carpeta raíz del proyecto, crea un nuevo archivo HTML y otro CSS:

```sh
$ touch gastronomia.html
$ touch css/gastronomia.css
```

## Paso 2: Editar el menú de navegación en index.html

Abre index.html y agrega un nuevo enlace en la barra de navegación:

```html
<nav>
  <ul>
    <li><a href="#">Inicio</a></li>
    <li><a href="#lugares">Lugares Icónicos</a></li>
    <li><a href="#cultura">Cultura y Tradiciones</a></li>
    <li><a href="gastronomia.html">Gastronomía</a></li>
  </ul>
</nav>
```

## Paso 3: Crear la estructura base de gastronomia.html

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Descubre México - Gastronomía</title>
    <link rel="stylesheet" href="./css/gastronomia.css" />
  </head>
  <body>
    <header>
      <img src="./img/jira.svg" alt="Chichén Itzá" width="50px" />
      <nav>
        <ul>
          <li><a href="index.html">Inicio</a></li>
          <li><a href="index.html#lugares">Lugares Icónicos</a></li>
          <li><a href="index.html#cultura">Cultura y Tradiciones</a></li>
          <li><a href="gastronomia.html">Gastronomía</a></li>
        </ul>
      </nav>
      <div class="actions">
        <a>Sign In</a>
      </div>
    </header>

    <main>
      <section class="gastronomia-banner">
        <h1>Sabores de México</h1>
        <p>Explora la riqueza gastronómica que hace de México un país único.</p>
      </section>

      <section class="platillos">
        <div class="card">
          <img src="./img/tacos.jpg" alt="Tacos" />
          <h2>Tacos</h2>
          <p>
            Uno de los platillos más representativos y versátiles de México.
          </p>
        </div>
        <div class="card">
          <img src="./img/mole.jpg" alt="Mole" />
          <h2>Mole</h2>
          <p>Una mezcla compleja de chiles, especias y chocolate.</p>
        </div>
        <div class="card">
          <img src="./img/pozole.jpg" alt="Pozole" />
          <h2>Pozole</h2>
          <p>Tradicional sopa mexicana hecha a base de maíz y carne.</p>
        </div>
      </section>
    </main>

    <footer>
      <p>&copy; 2025 Descubre México</p>
    </footer>
  </body>
</html>
```

## Paso 4: Crear los estilos en gastronomia.css

```css
body {
  font-family: "Arial", sans-serif;
  margin: 0;
  padding: 0;
  background-color: #fffaf5;
  color: #333;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #c1272d;
  position: fixed;
  width: 100%;
  top: 0;
  height: 75px;
}

header img {
  padding: 10px;
}

header .actions {
  background-color: #1d8b24;
  padding: 15px;
  color: #f4f4f4;
  cursor: pointer;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  padding: 15px;
  margin: 0;
}
nav ul li {
  margin: 0 10px;
}
nav ul li a {
  color: white;
  padding: 10px 20px;
  text-decoration: none;
  font-weight: bold;
}
nav ul li a:hover {
  background-color: #8b1d24;
  border-radius: 5px;
}

.gastronomia-banner {
  margin-top: 100px;
  text-align: center;
  background-color: #fefbf7;
  padding: 40px 20px;
}

.platillos {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  padding: 40px 20px;
}

.card {
  background-color: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
  text-align: center;
  max-width: 300px;
  margin: 20px;
}

.card img {
  width: 100%;
  border-radius: 10px;
}

footer {
  text-align: center;
  background-color: #333;
  color: white;
  padding: 15px;
  margin-top: 40px;
}
```
## Resultado esperado

Al hacer clic en “Gastronomía” en la barra de navegación de index.html, serás llevado a gastronomia.html, donde verás una nueva sección con contenido relevante y con el mismo estilo del sitio principal.
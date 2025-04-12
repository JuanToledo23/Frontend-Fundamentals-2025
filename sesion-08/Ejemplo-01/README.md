# 🧪 Ejemplo 01: Crear la estructura final del proyecto

---

## 🎯 Introducción

Ahora vamos a aplicar **transiciones y animaciones** a nuestro sitio **"Descubre México"** utilizando únicamente CSS.  
Estas técnicas permiten agregar movimiento y dinamismo sin necesidad de usar JavaScript, lo que mejora la experiencia del usuario y hace más atractivo el sitio.

Bien implementadas, estas transiciones pueden guiar al usuario, llamar su atención de forma sutil y transmitir modernidad.

---

## ✅ Objetivos

1. Crear una nueva página dentro del proyecto actual.
2. Maquetar esta página reutilizando la estructura base de la landing principal.
3. Preparar un archivo SCSS exclusivo para esta página.
4. Aplicar una primera transición visible en un botón con `:hover`.

---

## 🧰 Requisitos

- Tener instalado **Visual Studio Code**.
- Tener configurado **Sass (Dart Sass)** o utilizar la extensión Live Sass Compiler.
- Contar con la estructura base del proyecto *Descubre México*.

---

## 🛠 Desarrollo paso a paso

### 1. Crea una nueva página HTML

En tu terminal, dentro del directorio raíz del proyecto, ejecuta:

```bash
touch about.html
```

También crea un archivo SCSS exclusivo para esta nueva página:

```bash
cd scss
touch _about.scss
```

> Si tu archivo principal es `main.scss`, asegúrate de importar este nuevo archivo:

```scss
@use 'about' as *;
```

---

### 2. Estructura del proyecto actualizada

Tu estructura de carpetas debe verse así:

```
descubre-mexico/
├── index.html
├── about.html
├── style.css
├── output.css
├── scss/
│   ├── main.scss
│   ├── _global.scss
│   └── _about.scss
```

---

### 3. Crea el contenido base de `about.html`

Puedes reutilizar la estructura de `index.html` y modificar el contenido del `<main>` para trabajar con esta nueva sección:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link rel="stylesheet" href="./style.css" />
  <title>Sobre México</title>
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
    <section class="about-hero">
      <h1>Sobre México</h1>
      <p>Explora la riqueza cultural y natural del país desde una nueva perspectiva.</p>
      <button class="btn-explorar">Explorar ahora</button>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Descubre México</p>
  </footer>
</body>
</html>
```

---

### 4. Estilos en `_about.scss`

Ahora vamos a aplicar una transición suave en el botón `.btn-explorar`:

```scss
.about-page {
  margin-top: 100px;
  padding: 40px 20px;
  text-align: center;

  .about-hero {
    h1 {
      font-size: 36px;
      color: #c1272d;
      font-family: 'Alegreya', serif;
    }

    p {
      font-size: 18px;
      margin-bottom: 20px;
      color: #333;
    }

    .btn-explorar {
      padding: 12px 24px;
      background-color: #1d8b24;
      color: white;
      font-size: 16px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: background-color 0.3s ease-in-out;

      &:hover {
        background-color: #145c1a;
      }
    }
  }
}
```

---

## ✨ ¿Qué hicimos?

- Creamos una nueva página HTML (`about.html`) con una sección sencilla.
- Insertamos un **botón interactivo** con una transición en el color de fondo cuando el cursor pasa sobre él.
- Configuramos un archivo SCSS modular para mantener una buena organización del código.

---

## 📌 Resultado esperado

Cuando el usuario pasa el cursor sobre el botón **"Explorar ahora"**, este cambia suavemente de un verde claro a uno más oscuro, sin cortes bruscos.

Este es un primer paso para comenzar a añadir interactividad visual a la nueva sección de nuestro sitio.

---

📎 [Ir al Reto 01 → Agrega elementos a la nueva página](../reto-01/README.md)
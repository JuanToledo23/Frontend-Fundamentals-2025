# 🧪 Ejemplo 01: Crear la estructura final del proyecto

---

## 🎯 Introducción

Nuestro sitio **"Descubre México"** ya está muy avanzado. Ahora vamos a prepararlo para aplicar **transiciones y animaciones** utilizando únicamente CSS.  
Estas técnicas permiten agregar movimiento y dinamismo sin necesidad de usar JavaScript, lo que mejora la experiencia del usuario y hace más atractivo el sitio.

Bien implementadas, estas transiciones pueden guiar al usuario, llamar su atención de forma sutil y transmitir modernidad.

---

## ✅ Objetivos

1. Crear una nueva página dentro del proyecto actual.
2. Maquetar esta página reutilizando la estructura base de la landing principal.
3. Preparar un archivo SCSS exclusivo para esta página.
4. Comenzar a aplicar propiedades como `transition` y `animation`.

---

## 🧰 Requisitos

- Tener instalado **Visual Studio Code**.
- Tener configurado **Sass (Dart Sass)** o utilizar la extensión Live Sass Compiler.
- Contar con la estructura base del proyecto *Descubre México*.

---

## 🛠 Desarrollo paso a paso

### 1. Crea una nueva página HTML

Vamos a crear una nueva página llamada `about.html` para agregar y probar nuestras animaciones. En tu terminal, dentro del directorio raíz del proyecto, ejecuta:

```bash
touch about.html
```

También crea un archivo SCSS dedicado para esta nueva página:

```bash
cd scss
touch _about.scss
```

> Si tu archivo principal es `main.scss`, asegúrate de **importar** este nuevo archivo dentro de él:

```scss
@use 'about' as *;
```

---

### 2. Estructura del proyecto actualizada

Tu estructura de carpetas debería quedar así:

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

### 3. Nueva página base (about.html)

Puedes copiar la estructura de `index.html` y renombrar la sección principal para trabajar sobre ella:

```html
<main>
  <section class="about-hero">
    <h1>Sobre México</h1>
    <p>Explora la riqueza cultural y natural del país desde una nueva perspectiva.</p>
  </section>

  <section class="about-content">
    <!-- Aquí irán las tarjetas, imágenes o textos animados -->
  </section>
</main>
```

---

## ✨ Propiedades que usarás en esta sesión

Estas son las propiedades CSS que introduciremos:

- `transition`: para suavizar los cambios entre estados.
- `animation`: para definir animaciones complejas en CSS.
- `@keyframes`: para declarar cómo se comporta una animación en el tiempo.
- Pseudo-elementos y pseudo-clases como `:hover`, `:focus`, `::before`, `::after`.

---

## 💡 Ejemplo básico

```scss
.button {
  background-color: #c1272d;
  color: white;
  padding: 10px 20px;
  transition: background-color 0.3s ease;

  &:hover {
    background-color: #8b1d24;
  }
}
```

---

✅ Este es el inicio de la interactividad. En los siguientes retos y ejemplos iremos agregando transiciones, animaciones y efectos visuales enriquecedores dentro de esta nueva página.

---

📎 [Ir al Reto 01 → Agrega elementos a la nueva página](../reto-01/README.md)
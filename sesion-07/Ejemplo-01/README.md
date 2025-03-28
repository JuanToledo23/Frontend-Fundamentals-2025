# 🧪 Ejemplo 01: Empezando a estructurar Sass

---

## 🎯 Objetivos

- Establecer una estructura básica de archivos SCSS siguiendo buenas prácticas.
- Configurar el compilador de Sass para generar una hoja de estilos lista para producción.

---

## ✅ Requisitos previos

- Tener instalado **Visual Studio Code**.
- Tener instalado **Sass (versión Dart)** en tu sistema.  
  Puedes instalarlo siguiendo las instrucciones en [sass-lang.com/install](https://sass-lang.com/install)

---

## 🛠️ Desarrollo paso a paso

### 1. ¿SCSS o SASS?

Sass ofrece dos tipos de sintaxis:

- `.sass`: sintaxis indentada (no usa llaves ni punto y coma).
- `.scss`: sintaxis compatible con CSS (usa llaves y punto y coma).

Usaremos `.scss` porque es más cercana al CSS tradicional y más fácil de adoptar.

---

### 2. Estructura de carpetas

Vamos a crear una carpeta `scss` donde estará el código fuente en Sass. Tu proyecto debería verse así:

```
.
├── scss/
│   └── main.scss
├── index.html
├── output.css
├── styles.css
```

> El archivo `output.css` será generado automáticamente a partir del archivo Sass.  
> `styles.css` sigue siendo tu hoja de estilos principal. Puedes seguir usándola para otras secciones si lo deseas, o ir migrando todo a Sass progresivamente.

---

### 3. Escribiendo tu primer archivo `.scss`

Dentro de `scss/main.scss`, escribe lo siguiente:

```scss
.blog {
  background-color: #ffffff;
}
```

---

### 4. Compilando Sass

Abre tu terminal, navega a la raíz del proyecto y ejecuta este comando:

```bash
sass --watch scss/main.scss output.css
```

Este comando hace que Sass **monitoree** los cambios en `main.scss` y genere automáticamente el archivo `output.css` cada vez que guardes.

👉 Verás algo como esto en la terminal:

```
Compiled scss/main.scss to output.css.
Sass is watching for changes. Press Ctrl-C to stop.
```

---

### 5. Enlazando el CSS compilado a tu HTML

En tu archivo `index.html`, agrega un enlace al archivo `output.css`:

```html
<!-- index.html -->
<head>
  <!-- Aquí vienen los enlaces a Bootstrap y styles.css -->
  <link rel="stylesheet" href="./output.css" />
</head>
```

---

### 6. Agregando la sección del blog a la landing

Integra esta sección dentro del `<body>` de tu archivo `index.html`, justo antes del footer, o donde consideres que tiene sentido:

```html
<!-- Sección de Blog -->
<section class="blog">
  <h2>Explora nuestro blog</h2>
  <p>Descubre artículos sobre cultura, viajes y tradiciones mexicanas.</p>
</section>
```

Este bloque utilizará los estilos definidos en tu `main.scss`.

---

### 7. Verificando en el navegador

Abre el sitio en tu navegador e inspecciona con DevTools. Verás que la sección `.blog` tiene el fondo blanco como se definió en el archivo SCSS.

![Estilos de sass en el devtools](../assets/sass-devtools.png)

---

## 🎉 ¿Y ahora qué?

Acabamos de escribir SCSS y compilarlo exitosamente a CSS. ¿Notaste que el código se ve casi igual a CSS puro?  
La verdadera magia de Sass empieza cuando usamos **variables, mixins, estructuras y funciones**.  
¡Eso es justo lo que exploraremos a continuación!

---

📎 [Ir al Ejemplo 02 → Agregando la primera columna del blog](../Ejemplo-02/README.md)

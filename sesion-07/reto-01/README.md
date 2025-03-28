# 🧠 Reto 01: Agrega colores usados en las tarjetas

---

## 🎯 Objetivos

- Usar la DevTools del navegador para inspeccionar elementos.
- Agregar nuevas variables de color en tu archivo SCSS.
- Aplicar estos nuevos colores a los estilos de la sección del blog.

---

## ✅ Requisitos previos

- Tener instalado **Visual Studio Code**.
- Tener configurado Sass correctamente.
- Tener ya creada la carpeta `scss/` y los archivos `_global.scss` y `main.scss`.

---

## 🔍 Instrucciones

1. Abre tu navegador y utiliza la herramienta de desarrollador (DevTools) para **inspeccionar los colores** de texto, botones o fondos en la sección del blog.
2. Elige **dos nuevos colores** que puedas reutilizar para mejorar la sección del blog o las tarjetas.
3. Define estos colores como **variables SCSS** dentro de tu archivo `_global.scss`.
4. Usa esas variables dentro de `main.scss` para actualizar los estilos existentes o agregar nuevos.

---

## 💡 Tip

Si quieres experimentar con nuevas tipografías para la landing _Descubre México_, puedes consultar:

- [Google Fonts](https://fonts.google.com/)
- [FontPair](https://fontpair.co/)

Una vez que elijas tus fuentes, puedes agregarlas en el `<head>` de tu `index.html`:

```html
<link
  href="https://fonts.googleapis.com/css2?family=Playfair+Display&family=Open+Sans&display=swap"
  rel="stylesheet"
/>
```

Y luego definirlas como variables SCSS:

```scss
// _global.scss

// Fuentes
$font-title: "Playfair Display", serif;
$font-body: "Open Sans", sans-serif;
```

---

<details>
  <summary>💡 Posible solución</summary>

Agregar nuevas variables de color en `_global.scss`:

```scss
// _global.scss

$dark-green-title: #025157;
$dark-green-text: #135359;
$white: #ffffff;

// Nuevos colores propuestos
$gray: #4a4a4a;
$light-gray: #979797;
$light-green: #67b54b;
```

Luego puedes usar estas variables dentro de tus componentes en `main.scss`:

```scss
.card {
  background-color: $light-gray;
  color: $gray;
}
```

</details>

---

✅ ¡Listo! Este reto te ayudará a profesionalizar tu sistema de diseño en Sass, reutilizando colores de forma ordenada y eficiente.

---

📎 [Ir al Reto 02 → Agrega la tercera columna del blog](../reto-02/README.md)

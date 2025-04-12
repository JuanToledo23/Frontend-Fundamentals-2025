# 🧪 Ejemplo 02: Transiciones y pseudo-elementos

---

## 🎯 Introducción

Las **transiciones** permiten suavizar los cambios visuales que ocurren cuando un elemento cambia de estado, como al pasar el mouse por encima (`:hover`).  
Esto mejora la experiencia del usuario al hacer que los cambios visuales no sean bruscos, sino progresivos.

En este ejemplo vamos a aplicar una transición en **texto** y en un **botón**, directamente en la nueva página `about.html` del proyecto **"Descubre México"**.

---

## ✅ Objetivos

1. Usar `transition` para aplicar efectos suaves sobre texto y botones.
2. Detectar estados de interacción con `:hover`.
3. Entender cómo combinar múltiples transiciones en un mismo elemento.

---

## 🛠 Desarrollo paso a paso

### 1. Agrega contenido en `about.html`

Abre tu archivo `about.html` y agrega la siguiente sección debajo de `.about-hero`:

```html
<section class="about-content">
  <h2 class="section-title">¿Por qué visitar México?</h2>
  <p class="section-description">
    México es un país vibrante, lleno de cultura, gastronomía y paisajes que enamoran.
  </p>
  <button class="cta-button">Explorar Lugares</button>
</section>
```

---

### 2. Estilos en `_about.scss`

Ahora agrega los siguientes estilos a tu archivo `scss/_about.scss`:

```scss
.about-content {
  text-align: center;
  padding: 60px 20px;

  .section-title {
    font-size: 32px;
    color: #333;
    margin-bottom: 16px;
    transition: color 0.3s ease-in-out;

    &:hover {
      color: #c1272d; // Rojo tradicional mexicano
    }
  }

  .section-description {
    font-size: 18px;
    color: #444;
    margin-bottom: 30px;
    max-width: 600px;
    margin-left: auto;
    margin-right: auto;
  }

  .cta-button {
    background-color: #1d8b24;
    color: white;
    padding: 12px 24px;
    font-size: 16px;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    transition: background-color 0.3s ease-in-out;

    &:hover {
      background-color: #145c1a; // Verde más oscuro al hacer hover
    }
  }
}
```

---

### 3. ¿Qué hace exactamente `transition`?

La propiedad `transition` permite que un cambio de propiedad CSS ocurra de forma **gradual**.

```scss
transition: color 0.3s ease-in-out;
```

Esto significa:

- `color`: es la propiedad que va a cambiar.
- `0.3s`: el cambio durará 0.3 segundos.
- `ease-in-out`: comienza y termina lento, pero es más rápido en medio.

Puedes aplicar transiciones a muchas propiedades: `color`, `background-color`, `font-size`, `transform`, etc.

---

### 4. Resultado visual

📌 Estado inicial (sin interacción):  
- El título es gris oscuro.
- El botón es verde.

🖱️ Al pasar el cursor sobre el título o el botón:
- El título cambia a rojo.
- El botón cambia a un verde más intenso.

📸 Referencias visuales:
- ![Elemento base](../assets/elementoBase.png)
- ![Elemento con hover](../assets/elementoHover.png)

---

## 💡 Buenas prácticas: DRY (Don't Repeat Yourself)

Evita duplicar estilos. Si tienes varios botones que usan el mismo diseño, define una clase general (`.cta-button`) y reutilízala.

Así, cualquier ajuste en un solo lugar se reflejará en todos los botones del mismo tipo.

---

✅ Con este ejercicio ya estás aplicando interactividad real en tu sitio con **CSS puro**, sin necesidad de JavaScript.

---

📎 [Ir al Reto 02 → Agrega una nueva transición combinada](../reto-02/README.md)
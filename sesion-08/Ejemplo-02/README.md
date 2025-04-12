# 🧪 Ejemplo 02: Transiciones y pseudo-elementos

---

## 🎯 Introducción

Las **transiciones** permiten suavizar los cambios visuales que ocurren cuando un elemento cambia de estado, como al pasar el mouse por encima (`:hover`).  
Esto es útil para crear una experiencia más fluida y atractiva, en lugar de aplicar cambios bruscos.

En este ejemplo vamos a aplicar nuestra **primera transición en CSS**, utilizando texto y botones dentro de la nueva página `about.html` del proyecto **"Descubre México"**.

---

## ✅ Objetivos

1. Utilizar la propiedad `transition` en elementos `<button>` y `<h2>`.
2. Aplicar el pseudo-selector `:hover` para activar una transición visual.
3. Entender el uso de `transition` como propiedad abreviada.

---

## 🛠 Desarrollo paso a paso

### 1. Selecciona un elemento para animar

Vamos a aplicar una transición a los títulos de las tarjetas o a un botón dentro de la nueva sección `about.html`. Puedes usar el siguiente bloque de HTML como base:

```html
<section class="about-content">
  <h2 class="section-title">¿Por qué visitar México?</h2>
  <button class="cta-button">Explora Lugares</button>
</section>
```

---

### 2. Estilos SCSS con transición

En tu archivo `_about.scss`, agrega lo siguiente:

```scss
.section-title {
  font-size: 32px;
  color: #333;
  text-align: center;
  transition: color 0.3s ease-in-out;

  &:hover {
    color: #c1272d; // Cambia a un rojo mexicano al pasar el mouse
  }
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
```

---

### 3. ¿Qué hace exactamente `transition`?

La propiedad `transition` permite definir, en una sola línea, cómo se va a ejecutar un cambio visual en el elemento. Es una forma abreviada de:

- `transition-property`: Qué propiedad cambiará (por ejemplo, `color` o `background-color`)
- `transition-duration`: Cuánto tiempo durará la transición (por ejemplo, `0.3s`)
- `transition-timing-function`: Cómo será el ritmo del cambio (`ease-in`, `ease-out`, `linear`, etc.)
- `transition-delay` *(opcional)*: Cuánto tiempo esperar antes de iniciar la transición

---

### 4. Resultado visual

Cuando se carga la página, el botón y el título tienen su **estado base**.  
Al pasar el cursor sobre ellos, la transición se activa suavemente.

📸 Estado inicial:
![Elemento base](../assets/elementoBase.png)

📸 Estado con `:hover` activado:
![Elemento con hover](../assets/elementoHover.png)

---

## 💡 Buenas prácticas: DRY (Don't Repeat Yourself)

Reutiliza clases siempre que los elementos compartan los mismos estilos.  
Por ejemplo, si varios botones tienen la misma estructura visual, define una sola clase `.cta-button` y aplícala a todos. Así, un solo cambio en SCSS actualizará todos los botones del proyecto.

---

✅ Con esto ya estás aplicando interactividad básica a tu proyecto usando solo CSS, ¡sin una sola línea de JavaScript!

---

📎 [Ir al Reto 02 → Agrega una nueva transición](../reto-02/README.md)
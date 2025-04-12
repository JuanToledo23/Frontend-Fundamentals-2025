# 🧠 Reto 02: Agregando otra transición al elemento actual

---

## 🎯 Objetivos

1. Aplicar **más de una transición simultáneamente** sobre un mismo elemento.
2. Controlar la duración y el ritmo (timing) de cada transición para mejorar la experiencia visual.

---

## ✅ Requisitos

- Tener instalado **Visual Studio Code**.
- Haber creado y enlazado tu archivo `about.scss` al archivo `about.html`.
- Tener configurado el compilador de Sass (con Live Sass Compiler o vía terminal).

---

## 🛠 Instrucciones

Ahora que ya tienes una transición aplicada al color del texto, vas a mejorar la interacción visual **agregando también un cambio de tamaño de fuente** cuando el usuario pase el mouse (`:hover`).

Ambas propiedades (color y tamaño) deben:

- Cambiar suavemente usando `transition`.
- Tener **duraciones diferentes** para observar el comportamiento combinado.

---

## ✏️ ¿Dónde aplicarlo?

Puedes hacerlo sobre el título principal (`h1` o `.section-title`) o sobre el título de cada tarjeta (`h3`, `.feature__title`), dentro de la nueva página `about.html`.

---

## 💡 Tip

Para aplicar varias transiciones, puedes separarlas por coma:

```scss
transition: color 0.3s ease-in-out, font-size 0.5s ease-out;
```

También puedes usar `transition: all 0.4s ease-in-out;` si todas las transiciones usarán el mismo tiempo y función, pero **es preferible ser explícito** con cada propiedad si necesitas control total.

---

<details>
  <summary>💡 Posible solución</summary>

```scss
.feature__title {
  margin-top: 50px;
  font-weight: 500;
  font-size: 24px;
  font-family: 'Open Sans', sans-serif;
  margin-bottom: 35px;
  text-decoration: none;
  text-shadow: #025157 1px 1px 2px;

  transition: color 0.3s ease-in-out, font-size 0.5s ease-out;

  &:hover {
    color: #67b54b;
    font-size: 28px;
  }
}
```

</details>

---

✅ ¡Listo! Ahora tienes un título que cambia de color **y** de tamaño cuando el usuario pasa el cursor sobre él, creando un efecto más llamativo y profesional.

---

📎 [Ir al Reto 03 → Agrega una animación personalizada](../reto-03/README.md)
# 🧠 Reto 02: Agregando otra transición al elemento actual

---

## 🎯 Objetivos

1. Aplicar **más de una transición** sobre un mismo elemento usando CSS.
2. Controlar la **duración y ritmo** de cada transición por separado.
3. Reforzar el uso del pseudo-selector `:hover`.

---

## ✅ Requisitos

- Tener configurado **Visual Studio Code** y Sass.
- Haber creado los archivos `about.html` y `about.scss` y tenerlos vinculados correctamente.
- Haber completado el Ejemplo 02 con al menos una transición funcionando.

---

## 🛠 Instrucciones paso a paso

### 1. Modifica el HTML si es necesario

Verifica que en `about.html` exista un título como el siguiente:

```html
<section class="about-content">
  <h2 class="section-title">¿Por qué visitar México?</h2>
</section>
```

> Este será el elemento al que aplicaremos **más de una transición**.

---

### 2. Aplica múltiples transiciones en `_about.scss`

Ahora edita los estilos de `.section-title` para que tenga dos transiciones:

- Una al cambiar el **color** del texto.
- Otra al modificar el **tamaño** (`font-size`).

```scss
.about-content {
  .section-title {
    font-size: 32px;
    color: #333;
    transition: color 0.3s ease-in-out, font-size 0.5s ease;

    &:hover {
      color: #c1272d;
      font-size: 38px;
    }
  }
}
```

---

## ✅ Resultado esperado

- El título se ve normal al cargar la página.
- Al pasar el mouse sobre él (`:hover`), cambia:
  - De color: de gris a rojo.
  - De tamaño: de 32px a 38px.

Todo esto ocurre de forma suave y fluida gracias a las **transiciones combinadas**.

---

## 📌 Tip profesional

En lugar de usar `transition: all`, se recomienda declarar explícitamente las propiedades que deseas animar, así evitas efectos no deseados y tienes mayor control.

```scss
transition: color 0.3s ease-in-out, font-size 0.5s ease;
```

---

<details>
  <summary>💡 Posible variación</summary>

También puedes aplicar el mismo efecto sobre los títulos de las tarjetas (`h3`) para dar más dinamismo visual a las secciones informativas:

```scss
.feature h3 {
  transition: color 0.2s ease, transform 0.4s ease;

  &:hover {
    color: #1d8b24;
    transform: scale(1.1);
  }
}
```

</details>

---

📚 Con esto ya sabes cómo aplicar múltiples transiciones de forma profesional en tu sitio.

---

📎 [Ir al Reto 03 → Agrega una animación personalizada](../reto-03/README.md)
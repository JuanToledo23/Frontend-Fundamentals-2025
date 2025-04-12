# 🧠 Reto 03: Agregar una animación con CSS

---

## 🎯 Objetivos

1. Usar `@keyframes` para animar un elemento verticalmente con CSS.
2. Aplicar múltiples animaciones simultáneas en un solo elemento.
3. Comprender cómo usar `position`, `top`, `left` y `animation` de forma conjunta.

---

## ✅ Requisitos

- Tener configurado tu proyecto **"Descubre México"**.
- Tener creado y vinculado correctamente el archivo `about.scss`.
- Contar con el archivo `about.html` funcionando en navegador.

---

## 🛠 Instrucciones

Para cerrar esta sesión con broche de oro, vas a **animar una flecha** que:

- Se mueva de arriba hacia abajo (60px).
- Vuelva a su posición original en bucle.
- Opcional: también se mueva de izquierda a derecha.
- Se centre usando el sistema de columnas de Bootstrap.

---

## 📸 Resultado esperado

- Estado inicial:
  ![Estado inicial de la animación](../assets/flecha_animada.png)
- Imagen a utilizar:
  ![Flecha para animar](../assets/green-arrow.png)

🔽 Guarda la imagen `green-arrow.png` dentro de la carpeta `/img/` de tu proyecto.

---

## ✏️ Paso a paso

### 1. Agrega el HTML en `about.html`

Coloca esto dentro del `<main>` de tu archivo `about.html`, debajo de cualquier sección existente:

```html
<section class="arrow-wrapper">
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-md-4 text-center">
        <div class="flecha">
          <div class="flecha-contenedor">
            <div class="flecha-animada">
              <img src="./img/green-arrow.png" alt="Flecha animada" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
```

---

### 2. Agrega los estilos en `_about.scss`

Pega lo siguiente en tu archivo `scss/_about.scss`:

```scss
.arrow-wrapper {
  margin-top: 60px;
}

.flecha {
  margin: 0 auto;
  height: 130px;
  width: 130px;
  margin-bottom: 35px;

  .flecha-contenedor {
    position: relative;
    height: 150px;
    width: 150px;
    margin: 0 auto;

    .flecha-animada {
      position: absolute;
      animation-name: up-and-down;
      animation-duration: 3s;
      animation-timing-function: ease-in-out;
      animation-iteration-count: infinite;
      animation-direction: alternate;
      height: 130px;
      width: 130px;

      img {
        width: 100%;
        transform: rotate(-90deg); // Flecha apunta hacia abajo
      }
    }

    @keyframes up-and-down {
      0% {
        top: 0;
      }
      50% {
        top: 60px;
      }
      100% {
        top: 0;
      }
    }
  }
}
```

---

### 💡 ¿Quieres más dinamismo?

Agrega una segunda animación lateral (`left ↔ right`) al mismo elemento:

```scss
.flecha-animada {
  animation-name: up-and-down, side-slide;
  animation-duration: 3s, 4s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
  animation-timing-function: ease-in-out;

  @keyframes side-slide {
    from {
      left: -30px;
    }
    to {
      left: 30px;
    }
  }
}
```

> Así, tu flecha se moverá arriba/abajo y de lado a lado en bucle continuo.

---

## 🧠 ¿Qué aprendiste aquí?

- A usar `@keyframes` para definir estados de animación.
- Cómo aplicar múltiples animaciones a un mismo elemento.
- Cómo usar `position: relative` y `absolute` para tener control sobre los movimientos.

---

✅ ¡Listo! Ya tienes una animación atractiva y funcional que puedes reutilizar en cualquier sección del sitio.

---

📎 [Ir al Postwork → Aplica lo aprendido en una sección personalizada](../postwork/README.md)
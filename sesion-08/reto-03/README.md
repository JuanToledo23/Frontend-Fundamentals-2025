# 🧠 Reto 03: Agregar una animación con CSS

---

## 🎯 Objetivos

1. Usar `@keyframes` para crear una animación con movimiento en eje vertical.
2. Aplicar múltiples animaciones en un mismo elemento.
3. Comprender el uso combinado de `position`, `top`, `left` y `animation`.

---

## ✅ Requisitos

- Tener configurado tu proyecto de **"Descubre México"**.
- Tener instalado **Visual Studio Code**.
- Haber creado y vinculado correctamente el archivo `about.scss`.

---

## 🛠 Instrucciones

Para cerrar esta sesión, vas a agregar una flecha animada que:

- Se mueva hacia abajo (60px) y luego regrese a su posición original.
- Se posicione en el centro de la pantalla usando el sistema de columnas de Bootstrap.
- Incluya una segunda animación opcional que se mueva de izquierda a derecha.

---

### 📸 Resultado esperado

- Estado inicial:
  ![Estado inicial de la animación](../assets/flecha_animada.png)
- Elemento a usar:
  ![Flecha para animar](../assets/green-arrow.png)

Guarda la imagen `green-arrow.png` dentro de la carpeta `/img/` de tu proyecto.

---

## ✏️ Paso a paso

### 1. HTML para insertar la flecha en `about.html`

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

### 2. SCSS para animar la flecha en `about.scss`

```scss
.flecha {
  margin: 0 auto;
  height: 130px;
  width: 130px;
  margin-bottom: 35px;

  .flecha-contenedor {
    position: relative;
    height: 150px;
    width: 150px;
    margin-bottom: 65px;

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
        transform: rotate(-90deg); // Apunta hacia abajo
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

### 💡 ¿Quieres más movimiento?

Agrega una segunda animación horizontal (`left → right`) al mismo elemento:

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

---

## ✅ Consejos

- Usa `position: absolute` para mover elementos respecto a su contenedor padre con `position: relative`.
- Las propiedades `top`, `left`, `bottom`, `right` son útiles para animaciones simples.
- Aplica animaciones con propósito: no sobrecargues visualmente tu sitio.

---

📎 [Ir al Postwork → Aplicar lo aprendido en una sección personalizada](../postwork/README.md)
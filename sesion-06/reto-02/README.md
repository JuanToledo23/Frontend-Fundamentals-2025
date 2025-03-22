# Reto 02 - Agregar Carousel y la primera tarjeta

## Introducción

En este reto aprenderás a **insertar componentes dentro de otros** usando Bootstrap. Vamos a utilizar un componente de carrusel (`Carousel`) para mostrar casos de éxito, y dentro de cada diapositiva insertaremos tarjetas (`Card`) personalizadas. Este ejercicio te ayudará a comprender mejor la composición visual y cómo organizar contenido usando Bootstrap de forma más avanzada.

---

## Objetivos

- Configurar y personalizar dos componentes de Bootstrap: Carrusel y Tarjeta.
- Insertar contenido dentro de otros elementos con estructuras anidadas.
- Ajustar estilos CSS para lograr una apariencia atractiva y responsiva.

---

## Requisitos

- Tener Visual Studio Code instalado.
- Conocer qué es un framework de CSS.
- Saber cómo funciona la propiedad `position: absolute` en CSS.

---

## Desarrollo paso a paso

### Paso 1: Inserta una tarjeta dentro del carrusel

Reemplaza el contenido del primer `img` dentro del `Carousel` por el contenido de tu tarjeta personalizada. Ejemplo:

```html
<div class="carousel-item active">
  <!-- Tarjeta 1: Everly -->
  <div class="card">
    <img
      src="https://getmatcha.com/wp-content/uploads/2019/05/profile-headshot-square.png"
      class="card-img-top"
      alt="Everly"
    />
    <div class="card-body">
      <div class="card-circle everly">
        <img
          src="https://getmatcha.com/wp-content/uploads/2019/05/everly_logo_blue_v3_x60@2x.png"
          alt="Everly"
        />
      </div>
      <h4>Everly</h4>
      <h3>
        Early-Stage CPG Brand Increases Lead Conversion 20x, Ecommerce Revenue
        20%
      </h3>
      <div class="results">
        <img
          src="https://getmatcha.com/wp-content/themes/getmatcha/img/icon_cart.png"
          alt="Cart icon"
        />
        <p>22% of monthly revenue influenced by content</p>
      </div>
    </div>
    <div class="card-footer">
      <button>See Case Study</button>
    </div>
  </div>
</div>
```

### Paso 2: Agrega las dos tarjetas restantes

Repite el mismo patrón anterior en los otros `carousel-item`, remplazando las siguientes imágenes por tarjetas similares.

### Paso 3: Aplica estilos CSS personalizados

Agrega los siguientes estilos en tu archivo CSS para asegurar que las tarjetas tengan el tamaño, proporción y visual esperados:

```css
.success-stories .card {
  max-width: 370px;
  width: 100%;
  min-height: 600px;
  margin: 0 auto;
}

.success-stories .card img {
  max-height: 30vh;
  object-fit: cover;
}

.success-stories .card .card-body {
  max-width: 370px;
  width: 100%;
  position: relative;
  padding: 40px 1rem 1rem;
}

.success-stories .card .card-body h4 {
  color: #025157;
  font-size: 18px;
  font-weight: 600;
  line-height: 20px;
  margin-bottom: 12px;
  font-family: "Slabo 27px", serif;
}

.success-stories .card .card-body h3 {
  font-size: 25px;
  font-weight: 400;
  line-height: 30px;
  margin-bottom: 20px;
}

.success-stories .card .card-body .results {
  display: flex;
  justify-content: flex-start;
  align-items: center;
}

.success-stories .card .card-body .results img {
  width: 26px;
  margin-right: 20px;
}

.success-stories .card .card-body .results p {
  margin: 0;
}

.success-stories .card .card-footer button {
  display: block;
  margin-left: 0;
  border-radius: 5px;
  font-size: 13px;
  font-weight: 600;
  padding: 12px 20px;
  width: 100%;
  background-color: #025157;
  color: #fff;
  border: none;
}

.success-stories .card .card-footer {
  background-color: #ffffff;
  color: #fff;
  border: none;
}

.success-stories .card .card-body .card-circle {
  display: flex;
  align-items: center;
  position: absolute;
  top: -45px;
  right: 20px;
  width: 75px;
  height: 75px;
  border-radius: 50%;
  padding: 5px;
}

.success-stories .card .card-body .card-circle.everly {
  background-color: #f9da73;
  border: 5px solid #f9da73;
}

.success-stories .card .card-body .card-circle.everly img {
  object-fit: contain;
  width: 100%;
}
```

---

## Resultado esperado

Tu carrusel debe mostrar tres tarjetas personalizadas en lugar de imágenes simples. Cada tarjeta debe estar bien alineada, contener su contenido relevante y funcionar correctamente dentro del carrusel, con transiciones suaves y estilos coherentes.

---


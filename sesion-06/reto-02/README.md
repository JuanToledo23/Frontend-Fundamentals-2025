# Reto 02 - Agregar un carrusel de lugares turísticos

## Introducción

Vamos a utilizar un componente de carrusel (Carousel) para mostrar lugares turísticos representativos de México, y dentro de cada diapositiva insertaremos tarjetas (Card) personalizadas.

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
<section class="turismo-carousel">
  <h2>Destinos turísticos de México</h2>
  <div class="carousel-item active">
    <!-- Tarjeta 1: CDMX -->
    <div class="card">
      <img src="./img/cdmx.webp" class="card-img-top" alt="Ciudad de México" />
      <div class="card-body">
        <div class="card-circle cdmx">
          <img src="./img/cancun.jpg" alt="Imagen de Cancún" />
        </div>
        <h4>Ciudad de México</h4>
        <h3>
          Conoce una de las ciudades más vibrantes de América Latina, llena de
          historia, cultura y gastronomía.
        </h3>
        <div class="results">
          <img src="./img/chichenitza.jpeg" alt="Icono de Chichén Itzá" />
          <p>Visitada por más de 12 millones de turistas al año</p>
        </div>
      </div>
      <div class="card-footer">
        <button>Ver más</button>
      </div>
    </div>
  </div>
</section>
```

### Paso 2: Agrega las dos tarjetas restantes

Repite el mismo patrón anterior en los otros `carousel-item`, remplazando las siguientes imágenes por tarjetas similares.

### Paso 3: Aplica estilos CSS personalizados

Agrega los siguientes estilos en tu archivo CSS para asegurar que las tarjetas tengan el tamaño, proporción y visual esperados:

```css
.turismo-carousel .card {
  max-width: 370px;
  width: 100%;
  min-height: 600px;
  margin: 0 auto;
}

.turismo-carousel .card img {
  max-height: 30vh;
  object-fit: cover;
}

.turismo-carousel .card .card-body {
  max-width: 370px;
  width: 100%;
  position: relative;
  padding: 40px 1rem 1rem;
}

.turismo-carousel .card .card-body h4 {
  color: #025157;
  font-size: 18px;
  font-weight: 600;
  line-height: 20px;
  margin-bottom: 12px;
  font-family: "Slabo 27px", serif;
}

.turismo-carousel .card .card-body h3 {
  font-size: 25px;
  font-weight: 400;
  line-height: 30px;
  margin-bottom: 20px;
}

.turismo-carousel .card .card-body .results {
  display: flex;
  justify-content: flex-start;
  align-items: center;
}

.turismo-carousel .card .card-body .results img {
  width: 26px;
  margin-right: 20px;
}

.turismo-carousel .card .card-body .results p {
  margin: 0;
}

.turismo-carousel .card .card-footer button {
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

.turismo-carousel .card .card-footer {
  background-color: #ffffff;
  color: #fff;
  border: none;
}

.turismo-carousel .card .card-body .card-circle {
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

.turismo-carousel .card .card-body .card-circle.cdmx {
  background-color: #f9da73;
  border: 5px solid #f9da73;
}

.turismo-carousel .card .card-body .card-circle.cdmx img {
  object-fit: contain;
  width: 100%;
}
```

---

## Resultado esperado

Tu carrusel debe mostrar tres tarjetas personalizadas en lugar de imágenes simples. Cada tarjeta debe estar bien alineada, contener su contenido relevante y funcionar correctamente dentro del carrusel, con transiciones suaves y estilos coherentes.

---

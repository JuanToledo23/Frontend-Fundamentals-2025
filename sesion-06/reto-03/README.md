# Reto 03 - Agregar las dos tarjetas restantes al carrusel

En el reto anterior insertaste una tarjeta personalizada dentro del carrusel para mostrar un destino turístico. Ahora, continuarás personalizando ese carrusel agregando dos tarjetas adicionales que muestren otros lugares representativos de México.

## Objetivos

1. Concluir la personalización del componente Carrusel de Bootstrap.
2. Reforzar el uso de componentes anidados con Bootstrap.
3. Usar el componente Tarjeta (Card) para presentar contenido visual y textual.

## REQUISITOS

- Tener Visual Studio Code instalado

### Paso 1: Duplica la estructura de la tarjeta existente

Dentro del carrusel, duplica el siguiente bloque de código para crear los dos nuevos carousel-item:

```html
<div class="carousel-item">
  <!-- Tarjeta 2: Oaxaca -->
  <div class="card">
    <img src="./img/oaxaca.jpg" class="card-img-top" alt="Oaxaca" />
    <div class="card-body">
      <div class="card-circle oaxaca">
        <img src="./img/oaxaca-icono.png" alt="Icono de Oaxaca" />
      </div>
      <h4>Oaxaca</h4>
      <h3>
        Cultura, tradición y gastronomía se unen en uno de los destinos más
        ricos de México.
      </h3>
      <div class="results">
        <img src="./img/mezcal.png" alt="Icono de mezcal" />
        <p>Reconocido mundialmente por su mezcal y fiestas tradicionales.</p>
      </div>
    </div>
    <div class="card-footer">
      <button>Ver más</button>
    </div>
  </div>
</div>
```

Y otro similar para un tercer destino (ej. Tulum, Guanajuato, San Miguel de Allende, etc.)

### Paso 2: Crea las nuevas clases de estilo si lo deseas

Si cada tarjeta necesita un color de fondo distinto en su círculo (card-circle), puedes agregar estas clases a tu CSS:

```css
.turismo-carousel .card .card-body .card-circle.oaxaca {
  background-color: #f4d35e;
  border: 5px solid #f4d35e;
}
```

### Paso 3: Verifica el funcionamiento del carrusel

Si cada tarjeta necesita un color de fondo distinto en su círculo (card-circle), puedes agregar estas clases a tu CSS:

1. Asegúrate de que las tarjetas cambian correctamente al navegar en el carrusel.
2. Verifica que el contenido no se rompe en dispositivos móviles.
3. Si los botones de navegación del carrusel no aparecen, revisa si tienes correctamente implementado el componente Carousel desde Bootstrap.

### Resultado esperado

Tu carrusel debe mostrar ahora tres tarjetas diferentes, cada una con una imagen principal, un ícono decorativo, una descripción breve y un botón. Estas tarjetas deben navegar correctamente al dar clic en las flechas del carrusel.

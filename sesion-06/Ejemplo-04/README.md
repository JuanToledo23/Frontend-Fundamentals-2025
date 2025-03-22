## 🧪 Ejercicio 04 - Agregando otro componente de Bootstrap

### 📂 Introducción

En este ejercicio aprenderás a integrar y personalizar el componente **Button Group** (botonera) de Bootstrap dentro de tu proyecto _Descubre México_. Además, incorporarás **íconos SVG personalizados dentro de los botones**, utilizando rutas relativas en HTML. Esto te permitirá construir interfaces más visuales, limpias y profesionales.

---

### 🎯 Objetivos

1. Agregar el componente **button group** de Bootstrap.
2. Incluir imágenes SVG como íconos dentro de botones.
3. Aplicar rutas relativas para cargar recursos locales.

---

### 🛠️ Requisitos previos

- Tener instalado [Visual Studio Code](https://code.visualstudio.com/).
- Tener un proyecto con Bootstrap ya enlazado.
- Conocer la estructura básica de una página HTML.
- Saber cómo crear carpetas y archivos dentro de tu proyecto.

---

### 🧱 Desarrollo paso a paso

#### 1. Ubicar el lugar donde agregarás el componente

Dentro de tu archivo `index.html` (o una nueva página si prefieres), ubica la etiqueta `<main>` y asegúrate de que tiene una estructura clara.

Vamos a insertar la botonera dentro de un nuevo `<div>` que se colocará en esta área principal.

---

#### 2. Copiar la estructura básica del button group

Dirígete a la documentación oficial de Bootstrap:  
[https://getbootstrap.com/docs/5.1/components/button-group/#basic-example](https://getbootstrap.com/docs/5.1/components/button-group/#basic-example)

Copia el ejemplo básico de `button group` y pégalo en tu código, dentro de `<main>`:

```html
<div class="platforms">
  <h5>MI SITIO ESTÁ IMPULSADO POR</h5>
  <div class="btn-group" role="group" aria-label="Plataformas">
    <button type="button" class="btn btn-secondary">Shopify</button>
    <button type="button" class="btn btn-secondary">Wordpress</button>
    <button type="button" class="btn btn-secondary">Otra</button>
  </div>
</div>
```

---

#### 3. Crear la carpeta de íconos

En tu proyecto, crea una carpeta llamada:

```
/icons
```

Dentro de esta carpeta vas a guardar los íconos en formato `.svg`. Puedes descargar estos archivos desde internet (o usar los siguientes enlaces de ejemplo) y guardarlos con los siguientes nombres:

- `shopify.svg`
- `wordpress.svg`

> ⚠️ Asegúrate de que los archivos SVG estén bien formateados y que tengan dimensiones adecuadas para usarse como íconos (ej. 20x20px o 24x24px).

---

#### 4. Agregar los íconos dentro de los botones

Ahora modifica los botones para que incluyan una imagen SVG justo antes del texto. Utiliza la etiqueta `<img>` y la ruta relativa hacia los archivos:

```html
<div class="platforms">
  <h5>MI SITIO ESTÁ IMPULSADO POR</h5>
  <div class="btn-group" role="group" aria-label="Plataformas">
    <button type="button" class="btn btn-secondary">
      <img
        src="./icons/shopify.svg"
        alt="Icono de Shopify"
        width="24"
        height="24"
      />
      Shopify
    </button>
    <button type="button" class="btn btn-secondary">
      <img
        src="./icons/wordpress.svg"
        alt="Icono de Wordpress"
        width="24"
        height="24"
      />
      Wordpress
    </button>
    <button type="button" class="btn btn-secondary">Otra</button>
  </div>
</div>
```

> 🔍 _Tip_: Si el ícono se ve muy grande o muy pequeño, puedes ajustar su tamaño con los atributos `width` y `height`, o con clases de Bootstrap como `me-2` para darle espacio al texto.

---

### ✅ Resultado esperado

Tu componente final debería verse como una botonera horizontal con tres botones:

- Dos botones con íconos SVG personalizados (Shopify y Wordpress).
- Un tercer botón genérico.
- Todo alineado y estilizado con Bootstrap.

Además, los íconos deben cargarse correctamente desde la carpeta `/icons`.

---

### ⏭️ ¿Qué sigue?

En el siguiente ejercicio aprenderás a crear una **nueva página dentro del proyecto** que reutilice componentes como navbar, cards y botones, para mostrar un destino turístico específico. Esto te permitirá organizar tu sitio en múltiples secciones interconectadas y consistentes visualmente.

[Ir al siguiente ejercicio →](../Ejemplo-05/README.md)

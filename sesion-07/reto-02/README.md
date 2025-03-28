# 🧠 Reto 02: Agrega la tercera columna del blog

---

## 🎯 Objetivos

- Reutilizar los estilos aplicados previamente en la segunda columna (tarjeta de blog).
- Usar la consola de desarrollador (DevTools) para obtener información útil del diseño.
- Investigar sobre condicionales en Sass y cómo pueden mejorar la escritura de estilos.

---

## ✅ Requisitos previos

- Tener instalado **Visual Studio Code**.
- Tener configurado Sass y los archivos `_global.scss` y `main.scss`.
- Haber completado los ejemplos anteriores de la sección del blog.

---

## 🧱 Instrucciones

1. Duplica el contenido de la **segunda columna** (la tarjeta de blog) y colócalo dentro de la **tercera columna** (`<div class="col">` restante).
2. Cambia el contenido del post (imagen, título, autor, etc.) para que sea **único**.
3. Asegúrate de que se mantenga el mismo estilo reutilizando las clases existentes.
4. Usa las herramientas de inspección del navegador para verificar dimensiones, colores y tipografía, y ajusta tu SCSS si es necesario.

---

## 💡 Pregunta para reflexión

Hasta ahora hemos aprendido que Sass es más expresivo que CSS, y permite usar estructuras similares a lenguajes de programación.

### ❓ Pregunta:

> ¿Sass tiene condicionales `if`? ¿Cómo se usan?  
> ¿Es recomendable usarlos? ¿En qué casos los aplicarías?

Investiga y anota tu respuesta. Puedes consultar la [documentación oficial de Sass sobre condicionales](https://sass-lang.com/documentation/at-rules/control/if) como punto de partida.

Ejemplo básico:

```scss
$theme: light;

body {
  @if $theme == light {
    background-color: #ffffff;
    color: #222222;
  } @else {
    background-color: #222222;
    color: #ffffff;
  }
}
```

---

✅ Este tipo de lógica puede ayudarte a construir temas dinámicos o aplicar estilos condicionales según ciertas variables de configuración.

---

📎 [Ir al Postwork → Reforzando lo aprendido](../postwork/README.md)

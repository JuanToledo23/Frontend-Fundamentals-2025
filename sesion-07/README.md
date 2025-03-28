# 🎯 Sesión 07: Optimizando la producción de CSS

Bienvenido a la séptima sesión de **Front End Fundamentals**. Hoy daremos un gran paso hacia la escritura de **estilos más profesionales, organizados y reutilizables** usando un preprocesador de CSS llamado **Sass** (Syntactically Awesome Stylesheets).

---

## 🧠 Introducción

CSS es un lenguaje poderoso para aplicar estilos a los elementos HTML. Sin embargo, cuando los proyectos crecen, el código CSS puede volverse difícil de mantener.

Aquí es donde entran los **preprocesadores de CSS** como Sass y SCSS, los cuales nos permiten:

- Usar **variables**, **funciones**, **condicionales** y **bucles**.
- Separar el código en **módulos reutilizables**.
- **Optimizar** y **escalar** la producción de estilos CSS.

En esta sesión trabajaremos con **SCSS**, la sintaxis más amigable para quienes ya están familiarizados con CSS tradicional.

---

## 🚀 Objetivos de aprendizaje

Al finalizar esta sesión podrás:

- Entender qué es Sass y cómo se usa en proyectos reales.
- Escribir estilos usando la sintaxis SCSS.
- Organizar tu CSS en módulos reutilizables.
- Compilar SCSS a CSS utilizando herramientas como Dart Sass o extensiones de VS Code.
- Aplicar Sass a la estructura de columnas de blog de la página original de _Matcha_.

---

## 🧰 Requisitos

Antes de comenzar, asegúrate de tener lo siguiente instalado en tu entorno de desarrollo:

- **Visual Studio Code**
- Una de las siguientes opciones para compilar Sass:
  - [✅ Dart Sass](https://sass-lang.com/install)
  - [🧩 Live Sass Compiler Extension](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass) para Visual Studio Code

---

## 🗂️ Organización de la clase

| Tipo        | Actividad                                                                   | Duración estimada |
| ----------- | --------------------------------------------------------------------------- | ----------------- |
| 🧪 Ejemplo  | [Ejemplo 01: Empezando a estructurar Sass](./Ejemplo-01/README.md)          | 15 minutos        |
| 🧪 Ejemplo  | [Ejemplo 02: Agregando la primera columna del blog](./Ejemplo-02/README.md) | 25 minutos        |
| 🧪 Ejemplo  | [Ejemplo 03: Agregando la segunda columna del blog](./Ejemplo-03/README.md) | 15 minutos        |
| 🧠 Reto     | [Reto 01: Agrega colores usados en las tarjetas](./reto-01/README.md)       | 15 minutos        |
| 🧠 Reto     | [Reto 02: Agrega la tercera columna del blog](./reto-02/README.md)          | 25 minutos        |
| 🧩 Postwork | [Postwork - Práctica con Sass](./postwork/README.md)                        | —                 |

---

## 💡 Consejos

- Usa variables para almacenar colores, tamaños y fuentes que se repitan en el proyecto.
- Organiza tu código SCSS en **partials** (`_colores.scss`, `_layout.scss`, etc.) y luego **importa todo en un archivo principal** (`styles.scss`).
- Aprovecha los mixins para evitar repetición.
- Compila constantemente para ver cambios reflejados en el navegador.

---

## 🧭 ¿Qué sigue?

Después de esta sesión estarás listo para trabajar estilos de forma mucho más eficiente, modular y escalable.  
Lo aprendido con Sass te servirá no solo en proyectos personales, sino también en proyectos grandes o profesionales.

---

📎 [Volver al índice general del curso](../README.md)

# Documentación de TrummerWork (Beta v1)

## Introducción

Nos complace presentar TrummerWork, un proyecto desarrollado con el propósito de revolucionar la forma en que se construyen sitios web. TrummerWork es un framework CSS diseñado para ser simple, funcional y altamente adaptable para cualquier tipo de programador, desde principiantes hasta avanzados.

## Contenido

1. [Estilos Globales](#estilos-globales)
2. [Estilos para Textos](#estilos-para-textos)
3. [Estilos para Fondos](#estilos-para-fondos)
4. [Botones](#botones)
5. [CSS Grid](#css-grid)
6. [Barras de Navegación](#barras-de-navegación)
7. [Display: Flex](#display-flex)
8. [Estilos de Tarjetas](#estilos-de-tarjetas)
9. [Carruseles](#carruseles)
10. [Utilidades Responsivas](#utilidades-responsivas)

## Estilos Globales

### Importación de Fuentes

El framework importa varias fuentes de Google Fonts para ser utilizadas en el diseño:

```css
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Comfortaa:wght@300..700&family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900&family=Lora:ital,wght@0,400..700;1,400..700&family=Merriweather:ital,wght@0,300;0,400;0,700;0,900;1,300;1,400;1,700;1,900&family=Montserrat:ital,wght@0,100..900;1,100..900&family=Playfair+Display:ital,wght@0,400..900;1,400..900&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Raleway:ital,wght@0,100..900;1,100..900&family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&family=Slabo+27px&display=swap');
```

### Variables Globales

Define colores, fuentes y espaciado globales que se utilizan en todo el framework:

```css
:root {
    --colorgreen: #41B06E;
    --colorgreenHoover: #349159;
    --colorblueHover: #0E46A3;
    --colorblue: #175ac7;
    --colorRed: #C40C0C;
    --colorRedHover: #a00909;
    --colorYellow: #FFC100;
    --colorYellowHover: #b48802;
    --colorBlack: #151515;
    --colorBlackHover: #424242;
    --colorWhite: #ffffff;
    --colorWhiteHover: #c0c0c0;
    --colorGray: #B4B4B8;
    --colorGrayHover: #8a8a8a;
    --highlight-color: #e74c3c;
    --spacing-small: 8px;
    --spacing-medium: 16px;
    --spacing-large: 32px;
    --border-radius-small: 4px;
    --border-radius-medium: 8px;
    --border-radius-large: 16px;
    --font-primary: 'Montserrat', sans-serif;
    --font-secondary: 'Lato', sans-serif;
    --primary-color: #0E46A3;
    --secondary-color: #349159;
    --text-color: #424242;
}
```

## Estilos para Textos

### Tipografía

Define estilos para diferentes tipos de encabezados y párrafos:

```css
h1, h2, h3, h4, h5, h6 {
    color: var(--primary-color);
    margin-bottom: 0.5em;
}
h1 { font-size: 3.5em; }
h2 { font-size: 3.0em; }
h3 { font-size: 2.5em; }
h4 { font-size: 2.0em; }  
h5 { font-size: 1.5em; }
h6 { font-size: 1.25em; }

p { margin-bottom: 1.15em; }

a {
    color: var(--primary-color);
    text-decoration: none;
}
a:hover {
    color: var(--colorBlack);
    transition: 0.3s ease-in-out;
}
```

### Tipos de Textos

Define clases para diferentes estilos de texto y fuentes:

```css
.title-large { font-size: 2.5em; color: var(--colorBlack); }
.title-medium { font-size: 2em; color: var(--colorBlack); }
.title-small { font-size: 1.5em; color: var(--colorBlack); }
.subtitle { font-size: 1.25em; color: var(--secondary-color); }
.tw-p { font-size: 1.5em; color: var(--colorBlack); }
.tw-p-small { font-size: 0.875em; color: var(--text-color); }
.tw-cita-texto { font-size: 1.25em; color: var(--highlight-color); }
.text-resaltado { padding: 0.2em 0.4em; color: #fff; }
.text-resaltado-negro { background-color: var(--colorBlack); color: var(--colorWhite); }
.text-resaltado-azul { background-color: var(--colorblue); }
.text-shadow { text-shadow: 5px 2px 5px #151515; }
.text-minusculas { text-transform: uppercase; }
.text-mayusculas { text-transform: lowercase; }
.text-capitalizado { text-transform: capitalize; }
```

### Fuentes

Define clases para aplicar diferentes fuentes:

```css
.tw-mont { font-family: "Montserrat", sans-serif; }
.tw-lato { font-family: "Lato", sans-serif; }
.tw-lora { font-family: "Lora", serif; }
.tw-MeWa { font-family: "Merriweather", serif; }
.tw-slabo { font-family: "Slabo 27px", serif; }
.tw-popp { font-family: "Poppins", sans-serif; }
.tw-beNeu { font-family: "Bebas Neue", sans-serif; }
.tw-confor { font-family: "Comfortaa", sans-serif; }
.tw-raleway { font-family: "Raleway", sans-serif; }
```

## Estilos para Fondos

Define clases para aplicar colores de fondo:

```css
.bg-black { background-color: var(--colorBlack); }
.bg-white { background-color: var(--colorWhite); }
.bg-gray { background-color: var(--colorGray); }
.bg-red { background-color: var(--colorRed); }
.bg-green { background-color: #008000; }
.bg-blue { background-color: #0000ff; }
.bg-yellow { background-color: #ffff00; }
.bg-orange { background-color: #ffa500; }
.bg-purple { background-color: #800080; }
.bg-pink { background-color: #ffc0cb; }
.bg-brown { background-color: #a52a2a; }
.bg-teal { background-color: #008080; }
.bg-navy { background-color: #000080; }
.bg-olive { background-color: #808000; }
.bg-maroon { background-color: #800000; }
.bg-electric-blue { background-color: #007bff; }
.bg-neon-green { background-color: #39ff14; }
.bg-hot-pink { background-color: #ff69b4; }
.bg-sun-yellow { background-color: #ffdd00; }
.bg-orange-red { background-color: #ff4500; }
.bg-cyan { background-color: #00ffff; }
.bg-magenta { background-color: #ff00ff; }
.bg-lime { background-color: #00ff00; }
.bg-gold { background-color: #ffd700; }
.bg-turquoise { background-color: #40e0d0; }
.bg-coral { background-color: #ff7f50; }
.bg-indigo { background-color: #4b0082; }
.bg-emerald { background-color: #50c878; }
.bg-crimson { background-color: #dc143c; }
```

Claro, continúo con la documentación:

---

## Botones

Define estilos para diferentes tipos de botones:

```css
.boton {
    text-decoration: none;
    color: black;
    padding: 10px;
    border-radius: 10px;
    border: none;
    margin: 5px 0px;
    font-family: var(--font-primary);
    font-size: 1em;
    cursor: pointer;
    transition: background-color 0.3s ease, color 0.3s ease;
}

/* Botón primario */
.boton-primary {
    background-color: var(--primary-color);
    color: var(--colorWhite);
}
.boton-primary:hover {
    background-color: var(--colorblueHover);
}

/* Botón secundario */
.boton-secondary {
    background-color: var(--secondary-color);
    color: var(--colorWhite);
}
.boton-secondary:hover {
    background-color: var(--colorGreenHover);
}

/* Botón de alerta */
.boton-alert {
    background-color: var(--colorRed);
    color: var(--colorWhite);
}
.boton-alert:hover {
    background-color: var(--colorRedHover);
}

/* Botón de éxito */
.boton-success {
    background-color: var(--colorGreen);
    color: var(--colorWhite);
}
.boton-success:hover {
    background-color: var(--colorGreenHover);
}

/* Botón de advertencia */
.boton-warning {
    background-color: var(--colorYellow);
    color: var(--colorBlack);
}
.boton-warning:hover {
    background-color: var(--colorYellowHover);
}
```

## CSS Grid

Utiliza el sistema de cuadrícula (grid) para crear diseños flexibles y responsivos:

```css
/* Contenedor del grid */
.grid-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: var(--spacing-medium);
}

/* Elemento del grid */
.grid-item {
    background-color: var(--colorWhite);
    border: 1px solid var(--colorGray);
    padding: var(--spacing-small);
    border-radius: var(--border-radius-small);
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
}

/* Ejemplo de grid en un contenedor de 2 columnas */
.grid-2-cols {
    grid-template-columns: repeat(2, 1fr);
}
```

## Barras de Navegación

Estilos para crear barras de navegación horizontal y vertical:

```css
/* Barra de navegación horizontal */
.navbar {
    display: flex;
    background-color: var(--primary-color);
    padding: var(--spacing-small);
    justify-content: space-between;
    align-items: center;
    border-bottom: 2px solid var(--colorGray);
}

.navbar a {
    color: var(--colorWhite);
    padding: var(--spacing-small);
    text-decoration: none;
    font-family: var(--font-secondary);
}

.navbar a:hover {
    background-color: var(--colorBlack);
    border-radius: var(--border-radius-small);
}

/* Barra de navegación vertical */
.sidebar {
    display: flex;
    flex-direction: column;
    background-color: var(--primary-color);
    padding: var(--spacing-small);
    width: 250px;
    height: 100vh;
    position: fixed;
    top: 0;
    left: 0;
    border-right: 2px solid var(--colorGray);
}

.sidebar a {
    color: var(--colorWhite);
    padding: var(--spacing-small);
    text-decoration: none;
    font-family: var(--font-secondary);
}

.sidebar a:hover {
    background-color: var(--colorBlack);
    border-radius: var(--border-radius-small);
}
```

## Display: Flex

Utiliza Flexbox para diseñar y alinear elementos de forma flexible:

```css
/* Contenedor Flex */
.flex-container {
    display: flex;
    flex-wrap: wrap;
    gap: var(--spacing-medium);
}

/* Elementos Flex */
.flex-item {
    flex: 1;
    min-width: 200px;
    background-color: var(--colorWhite);
    padding: var(--spacing-small);
    border: 1px solid var(--colorGray);
    border-radius: var(--border-radius-small);
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
}

/* Alineación central */
.flex-center {
    justify-content: center;
    align-items: center;
}
```

## Estilos de Tarjetas

Diseña tarjetas para mostrar contenido en bloques:

```css
/* Tarjeta básica */
.card {
    background-color: var(--colorWhite);
    border: 1px solid var(--colorGray);
    border-radius: var(--border-radius-medium);
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
    padding: var(--spacing-medium);
    margin: var(--spacing-medium) 0;
}

/* Tarjeta con imagen */
.card-image {
    border-radius: var(--border-radius-medium);
    overflow: hidden;
    margin-bottom: var(--spacing-small);
}

.card-image img {
    width: 100%;
    height: auto;
}

/* Contenido de la tarjeta */
.card-content {
    font-family: var(--font-secondary);
}
```

## Carruseles

Estilos básicos para un carrusel de imágenes o contenido:

```css
/* Contenedor del carrusel */
.carousel {
    position: relative;
    overflow: hidden;
}

/* Elementos del carrusel */
.carousel-item {
    display: none;
    width: 100%;
    height: auto;
}

/* Mostrar el item activo */
.carousel-item.active {
    display: block;
}

/* Controles del carrusel */
.carousel-control {
    position: absolute;
    top: 50%;
    width: 40px;
    height: 40px;
    background-color: var(--primary-color);
    color: var(--colorWhite);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    transform: translateY(-50%);
    transition: background-color 0.3s ease;
}

.carousel-control:hover {
    background-color: var(--colorblueHover);
}

.carousel-control-prev {
    left: 10px;
}

.carousel-control-next {
    right: 10px;
}
```
## Conclusión

Esta documentación proporciona una guía práctica y directa para utilizar el framework Tumorwork. Puedes ajustar los estilos y clases según tus necesidades y personalizar el framework para que se adapte a tu proyecto. Si tienes alguna pregunta adicional o necesitas más ayuda, no dudes en consultar la documentación más detallada o buscar soporte adicional. 
Si tienes alguna sugerencia o duda te invitamos a escribir al mail: trummerwork@outlook.com
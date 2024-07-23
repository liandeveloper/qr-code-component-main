# Frontend Mentor - QR Code Component Solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of Contents

- [Frontend Mentor - QR Code Component Solution](#frontend-mentor---qr-code-component-solution)
  - [Table of Contents](#table-of-contents)
  - [Overview](#overview)
    - [Screenshot](#screenshot)
    - [Links](#links)
  - [My Process](#my-process)
    - [HTML Document Setting](#html-document-setting)
    - [Document Structure Body](#document-structure-body)
    - [Colors](#colors)
    - [CSS reset](#css-reset)
    - [Body](#body)
    - [Main](#main)
    - [QR Image](#qr-image)
    - [Information](#information)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Useful resources](#useful-resources)
  - [Author](#author)
  - [Acknowledgments](#acknowledgments)

## Overview

How to develoment a QR code card with HTML and CSS.

### Screenshot

![](readme/preview-desktop.png)

### Links

- Solution URL: [Add solution URL here](https://github.com/liandeveloper/qr-code-component-main)
- Live Site URL: [Add live site URL here](https://liandeveloper.github.io/qr-code-component-main/)

## My Process

### HTML Document Setting

**HTML Preview**:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- displays site properly based on user's device -->
    <!-- Favicon -->
    <link rel="icon" type="image/png" sizes="32x32" href="./images/favicon-32x32.png">
    <!-- Styles -->
    <link rel="stylesheet" href="styles.css">
    <!-- Outfit Font -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@100..900&display=swap" rel="stylesheet">
    <title>Frontend Mentor | QR code component</title>
  </head>
  <body>

  </body>
</html>
```

### Document Structure Body

**HTML Preview**:

```html
  <body>
    <!-- *Main -->
    <main class="main">

      <!-- *QR Image -->
      <section class="img">
        <!-- Image -->
        <img src="images/image-qr-code.png" alt="">
      </section>

      <!-- *Information -->
      <section class="info">
        <!-- Title -->
        <h2>Improve your front-end skills by building projects</h2>
        <!-- Description -->
        <h3>Scan the QR code to visit Frontend Mentor and take your coding skills to the next level</h3>
      </section>

    </main>
  </body>
```

**Preview**:

![QR HTML](readme/qr-html.png)

### Colors

**CSS Preview**:

```css
:root {
    /* Colors */
    --White: hsl(0, 0%, 100%);
    --Light-gray: hsl(212, 45%, 89%);
    --Grayish-blue: hsl(220, 15%, 55%);
    --Dark-blue: hsl(218, 44%, 22%);
}
```

> **Note**: ``:root`` is a pseudo-class selector used to select the root element of the document. By defining variables in ``:root``, you ensure that they are accessible throughout the document, which facilitates management and consistency of styles across the website.

### CSS reset

**CSS Preview**:

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

The `*` element will remove margins and padding from the elements and will conform to the box model to make it easier to control the size of the elements.

> **Nota**: ``*`` se llama «selector universal». Este selector se utiliza para aplicar estilos a todos los elementos de una página web, independientemente de su tipo.

### Body

**CSS Preview**:

```css
body {
    width: 100%;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: .5rem 0;
    font-family: "Outfit", sans-serif;
    font-weight: 400;
    font-size: 15px;
    background-color: var(--Light-gray);
}
```

The content of the `body` elements will be centered both vertically and horizontally, will apply a font with a specific size and weight, and a background color.

### Main

**CSS Preview**:

```css
/* *Main */
.main {
    width: 90%;
    max-width: 330px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1.5rem;
    padding: 1rem 0;
    background-color: var(--White);
    box-shadow: 10px 10px 30px -15px #000;
    overflow: hidden;
    border-radius: 1rem;
}
```

The element with class `.main` will have a flexible but limited width, its child elements will be vertically aligned and centered with spaces between them, they will also have vertical padding, a background color, shadow and rounded edges, while avoiding content overflow.

### QR Image

**HTML Preview**:

```html
<!-- *QR Image -->
<section class="img">
  <!-- Image -->
  <img src="images/image-qr-code.png" alt="">
</section>
```

**CSS Preview**:

```css
/* *QR Image */
.img {
    width: 90%;
    overflow: hidden;
    border-radius: 1rem;
}
/* Image */
.img img {
    width: 100%;
    display: block;
}
```

The `.img` container will be 90% of the `.main` width with rounded edges and will prevent the content from overflowing. The `.img` (image) tag will wrap the container as a block, which will eliminate any whitespace.

**Preview**:

![QR-Image](readme/qr-image.png)

### Information

**HTML Preview**:

```html
<!-- *Information -->
<section class="info">
  <!-- Title -->
  <h2>Improve your front-end skills by building projects</h2>
  <!-- Description -->
  <h3>Scan the QR code to visit Frontend Mentor and take your coding skills to the next level</h3>
</section>
```

**CSS Preview**:

```css
/* *Information */
.info {
    width: 90%;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
    text-align: center;
}
/* Title */
.info h2 {
    width: 95%;
    color: var(--Dark-blue);
}
/* Description */
.info h3 {
    width: 100%;
    font-weight: 400;
    color: var(--Grayish-blue);
}
```

The element with class `.info` will have a flexbox container with elements (children) in vertical direction and centered with spaces between them. The `h2` and `h3` elements will have specific sizes and colors, but `h3` will have a lighter font weight.

**Preview**:

![QR-Image](readme/qr-text.png)

****

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Mobile-first workflow

### What I learned

When creating a web page, it is essential to use semantic HTML to properly structure the parts of the document. In addition, Flexbox simplifies the task of organizing the elements on the page.

### Useful resources

- [Google Fonts](https://fonts.google.com/?preview.layout=grid) - It is a free library of web fonts that allows developers to integrate various fonts into their sites.

- [Visual Studio Code](https://code.visualstudio.com/) - It is a free and open source code editor developed by Microsoft for programmers and developers.

## Author

- Frontend Mentor - [@liandeveloper](https://www.frontendmentor.io/profile/liandeveloper)
- X - [@lian_dev](https://x.com/lian_dev)

## Acknowledgments

Thank you Frontend Mentor for your challenges that help to improve the ability to develop and design web pages.

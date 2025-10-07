# 🚀 Recipe Page

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

## Welcome! 👋

This project is my solution to the "Recipe Page" from Frontend Mentor. The goal was to build the optimal layout for the site depending on their device's screen size that closely matches the provided design.

Original challenge [Recipe page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm).

Part of the [Learning Path](https://www.frontendmentor.io/learning-paths) on Frontend Mentor.

![Design preview for the Recipe Page coding challenge](./assets/images/preview.jpg)

## 📋 Table of contents

- [Built with](#-built-with)
- [Live Preview](#-live-preview)
- [What I Learned](#-what-i-learned)
- [Author](#-author)
- [Acknowledgments](#-acknowledgments)

## 🛠 Built with

- **HTML5**: Semantic markup for structure and accessiblity.
- **CSS3**: Modern styling with Flexbox, and custom properties.
- **BEM Methodology**: Naming convention for scalable CSS.

## 🔗 Live Preview

[![Live Preview](https://img.shields.io/badge/Demo-Live-00BCD4?style=for-the-badge)](https://amansgz.github.io/recipe-page)

## 📚 What I Learned

### Font Implementation with @font-face

- **Multiple Font Families**: Implemented two distinct font families using `@font-face` rule
- **Font Weight Managment**: Configured different font weights for each font family

```css
/* fonts.css */
@font-face {
  font-family: "Outfit";
  src: url(./assets/fonts/outfit/static/Outfit-Regular.ttf) format(truetype);
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: "Outfit";
  src: url(./assets/fonts/outfit/static/Outfit-SemiBold.ttf) format(truetype);
  font-weight: 600;
  font-style: normal;
  font-display: swap;
}
```

### Generic Utility Classes

- **Sections Headings**: Created reusabled heading classes.

```css
/* Section Headings (Common styles) */
.recipe__subtitle {
  font-family: var(--ff-heading);
  font-size: var(--fs-heading-2);
  font-weight: 400;
  color: var(--clr-brown-800);
  margin-block-end: var(--spacing-100);
}
```

- **Lists**: Removing default list styles to create custom list styles.

```css
/* Common Lists */
.list {
  list-style: none;
  padding-inline-start: 0;
}
.list li {
  position: relative;
  padding-inline-start: var(--spacing-200);
  margin-block-end: var(--spacing-50);
  line-height: 1.5;
}
```

### List Styling

- **Custom List Indicators**: Created custom bullets and counter list using pseudo-elements(`::before`)

```css
.list li::before {
  content: ".";
  font-size: 2rem;
  position: absolute;
  inset-inline-start: 0;
  inset-block-start: -20px;
}

/* Rose Bullets List */
.list--time li::before {
  color: var(--clr-rose-800);
}

/* Brown Bullets List */
.list--ingredients li::before {
  color: var(--clr-brown-800);
}
```

```css
/* Ordered List */
.list--instructions {
  counter-reset: orderedList;
}
.list--instructions li {
  counter-increment: orderedList;
  margin-block-end: 10px;
  padding-inline-start: 30px;
  position: relative;
}
.list--instructions li::before {
  content: counter(orderedList) ".";
  font-size: var(--fs-body);
  font-weight: var(--fw-semibold);
  color: var(--clr-brown-800);
  position: absolute;
  inset-inline-start: 0;
  inset-block-start: 0;
}
```

## 👩‍💻 Author

- Frontend Mentor - [@amansgz](https://www.frontendmentor.io/profile/amansgz)
- Github - [@amansgz](https://www.github.com/amansgz)

## 🙌 Acknowledgments

- Challenge provided by [Frontend Mentor](https://www.frontendmentor.io).

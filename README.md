# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshot - Desktop

![](./images/image-product-desktop.jpg)

### Screenshot - Mobile

![](./images/image-product-mobile.jpg)

### Links

- Solution URL: [https://github.com/Grill3dCheese/FEM-ProductCard](https://github.com/Grill3dCheese/FEM-ProductCard)
- Live Site URL: [https://grill3dcheese.github.io/FEM-ProductCard/](https://grill3dcheese.github.io/FEM-ProductCard/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

This project was loads of fun and helped me learn/understand several things:

- Continued the mindset of first working on the HTML structure first and styling afterward
- Implemented a CSS reset file for the first time 🙌
- Gained a better understanding of when to use CSS Grid VS. Flexbox
- Used semantic HTML structuring elements: main, article and footer
- Learned all about the HTML <picture> element and implemented into this project
- Also learned about the HTML <del> element, how to use it AND issues with accessibility that can be resolved with some CSS magic! 🪄

```html
<picture>
  <source
    srcset="./images/image-product-desktop.jpg"
    media="(min-width: 640px)"
  />
  <img
    src="./images/image-product-mobile.jpg"
    alt="Gabrielle Essence Parfum bottle laying down with leaves surrounding"
  />
</picture>

<del>
  <p>$169.99</p>
</del>
```

```css
del::before,
del::after {
  clip-path: inset(100%);
  clip: rect(1px, 1px, 1px, 1px);
  height: 1px;
  overflow: hidden;
  position: absolute;
  white-space: nowrap;
  width: 1px;
}

del::before {
  content: " [deletion start] ";
}

del::after {
  content: " [deletion end] ";
}
```

### Continued development

- Continue working with CSS grid and Flexbox to understand how each work and when to use one VS. the other.

- Also continue to work on mobile-first workflow, remembering to start with the mobile viewport size(s) and work up from there.

### Useful resources

- [<picture>: The Picture element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture) - Excellent article from MDN explaining the use cases for the <picture> element and how it assists when using multiple images that display based on viewport size. Also explains fallbacks - where we can offer alternative image formats for cases where certain formats are not supported and how we can help to save bandwidth and improve page load times! A win-win!
- [<del>: The Deleted Text element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/del) - This is an amazing article which helped me finally understand the <del> HTML element. I originally started the project by using CSS to line-through the text. I shortly realized that there was an HTML element that could do this without needing HTML and is better for accessability purposes.

## Author

- Website - [Keith McKenna](https://www.keithmckenna.com)
- Frontend Mentor - [@Grill3dCheese](https://www.frontendmentor.io/profile/Grill3dCheese)
- Twitter - [@keithmckenna](https://www.twitter.com/keithmckenna)

## Acknowledgments

Thank you SO much to MDN for always coming in clutch on helping whenever I need explanations for any/everything! Oftentimes, questions arise while I'm coding and I know I can always count on MDN to fully explain down to the nitty gritty!

Also to Josh Comeau for the CSS reset instructions.

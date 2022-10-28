# Frontend Mentor - FAQ accordion card solution

This is a solution to the [FAQ accordion card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/faq-accordion-card-XlyjD0Oam). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Frontend Mentor - FAQ accordion card solution](#frontend-mentor---faq-accordion-card-solution)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
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

This is my solution to the Accordion Card Component challenge. It is a faq
accordion card component where the questions are visible and the user can click
on a question to expand it and reveal the answer.

### Screenshot

![](./src//assets//images//screenshot-desktop.png)
![](./src//assets//images/screenshot-mobile.png)

### Links

- Solution URL: [GitHub](https://github.com/newbpydev/09-faq-accordion-card-vue-typescript)
- Live Site URL: [Live Site](https://teal-sopapillas-2dd445.netlify.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Vue + Vite + TypeScript

### What I learned

I have learned how to use the background-image on divs with roles of imgs to be
able to control the image based on the media breakpoints. I have also learned
how to use a pseudo element to create a shadow behind isometric images.

```css
.faq::before {
  content: "";
  position: absolute;
  top: 20.3rem;
  left: -4.8rem;
  height: 15rem;
  width: 19.1rem;
  z-index: 99;

  background-image: url("@/assets/images/illustration-box-desktop.svg");
}
.faq::after {
  content: "";
  position: absolute;
  top: 18rem;
  left: 0.3rem;
  width: 9rem;
  height: 0rem;
  box-shadow: 0 12rem 3.5rem 0.5rem rgb(0 0 0);
}
```

### Continued development

For future development, I will continue to use pseudo elements to create the
desired design layouts. I will take more time to analize the layouts and
separate the layouts based on their elements.

### Useful resources

- [Medium - Absolute Centering in CSS](https://medium.com/front-end-weekly/absolute-centering-in-css-ea3a9d0ad72e) - input elements of type button are rendered as simple push buttons, which can be programmed to control custom functionality anywhere on a webpage as required when assigned an event handler function (typically for the click event).
- [MDN - Flexbox](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox) - Flexbox is a one-dimensional layout method for arranging items in rows or columns. Items flex (expand) to fill additional space or shrink to fit into smaller spaces. This article explains all the fundamentals.

## Author

- Website - [Juan Gomez](https://www.newbpydev.com)
- Frontend Mentor - [@newbpydev](https://www.frontendmentor.io/profile/newbpydev)
- Twitter - [@Newb_PyDev](https://twitter.com/Newb_PyDev)

## Acknowledgments

The code may not be perfect compared to my sensei @jonasschmedtman but I need
to thank him because he has shown me the ropes and now I am a confident web
designer.

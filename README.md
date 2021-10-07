# Frontend Mentor - Social proof section solution

This is a solution to the [Social proof section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/social-proof-section-6e0qTv_bA). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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


## Overview

### The challenge

Users should be able to:

- View the optimal layout for the section depending on their device's screen size

### Screenshot

![](./images/screenshot.jpg)


### Links

- Solution URL: [https://github.com/gchristofferson/social-proof-section](https://github.com/gchristofferson/social-proof-section)
- Live Site URL: [https://social-proof-section-eight-delta.vercel.app/](https://social-proof-section-eight-delta.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow


### What I learned

In this project I learned how to add multiple background images to the same element.  I had struggled with this previously, but in this project I think I finally nailed it.  The main background of the social proof section has a decorative .svg image in the upper left and lower right corners where I was able to practice this technique.

This is the code that adds the two images to the background in their proper positions:

```css
.body {
  background-image: url("../images/bg-pattern-top-mobile.svg"),
  url("../images/bg-pattern-bottom-mobile.svg");
  background-repeat: no-repeat,
  no-repeat;
  background-position: top left,
  bottom right;
}
```
The main thing to remember when adding multiple backgrounds is to add the background properties as a list and in the same order.

### Continued development

This project included interesting offset positioning of the review and testimonial boxes.  I offset them by first setting the position to relative for all boxes and then by selecting the appropriate :nth-child(). I then adjusted the bottom or left positioning. I'm sure there is a more elegant solution and I'd like to explore this more in future projects.

### Useful resources

- [https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Backgrounds_and_Borders/Using_multiple_backgrounds](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Backgrounds_and_Borders/Using_multiple_backgrounds) - This resource from the Mozilla Developer Network really helped me understand how to properly add multiple backgrounds to the same element. I really liked the straight forward explanations and code examples.

## Author

- Frontend Mentor - [@gchristofferson](https://www.frontendmentor.io/profile/gchristofferson)
- Twitter - [@GreggChristoff2](https://twitter.com/GreggChristoff2)


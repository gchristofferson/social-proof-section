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
- [Acknowledgments](#acknowledgments)


## Overview

### The challenge

Users should be able to:

- View the optimal layout for the section depending on their device's screen size

### Screenshot

![](./images/screenshot.jpg)


### Links

- Solution URL: [https://github.com/gchristofferson/social-proof-section/tree/flexbox-alignment-test](hhttps://github.com/gchristofferson/social-proof-section/tree/flexbox-alignment-test)
- Live Site URL: [https://social-proof-section-928xy06ss-gchristofferson.vercel.app/](https://social-proof-section-928xy06ss-gchristofferson.vercel.app/)

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

I also had a chance to practice aligning and offsetting boxes using flexbox align-self property.  What I learned is that for this to work, I need to set a height or width on the flex container that is higher or wider than the child elements within.  This then gives the necessary space within the container to offset individual elements using align-self.

Here's an example of where I set the height for the social ratings flex container:
```css

/* the flex container */
.social-ratings {
        display: flex;
        flex-direction: column;
        width: 540px;
        align-items: center;
    }

/* the flex items */
.social-rating {
  max-width: 445px;
}

/* the offset flex items */
.social-rating:nth-last-child(1) {
  align-self: flex-end;
}

.social-rating:nth-last-child(3) {
  align-self: flex-start;
}
```

### Continued development

This project included interesting offset positioning of the review and testimonial boxes.  I offset them by first setting the position to relative for all boxes and then by selecting the appropriate :nth-child(). I then adjusted the bottom or left positioning. I'm sure there is a more elegant solution and I'd like to explore this more in future projects.

Also, in future projects I think I'll set a default wrapper class with `display: flex` set and then I will add modifier classes so I can adjust width or height, depending on what the design needs.

### Useful resources

- [https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Backgrounds_and_Borders/Using_multiple_backgrounds](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Backgrounds_and_Borders/Using_multiple_backgrounds) - This resource from the Mozilla Developer Network really helped me understand how to properly add multiple backgrounds to the same element. I really liked the straight forward explanations and code examples.

## Author

- Frontend Mentor - [@gchristofferson](https://www.frontendmentor.io/profile/gchristofferson)
- Twitter - [@GreggChristoff2](https://twitter.com/GreggChristoff2)

## Acknowledgments

I'd like to tip my had to [@erelita](https://www.frontendmentor.io/profile/erelita) who helped me fix my flexbox alignment issue!
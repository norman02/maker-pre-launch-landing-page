# Frontend Mentor - Maker pre-launch landing page solution

This is a solution to the [Maker pre-launch landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/maker-prelaunch-landing-page-WVZIJtKLd). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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
- [Acknowledgements](#Acknowledgements)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements
- Receive an error message when the form is submitted if:
  - The `Email address` field is empty should show "Oops! Please add your email"
  - The email is not formatted correctly should show "Oops! That doesn’t look like an email address"

### Screenshot

![](./screenshot.png)


### Links

- Solution URL: [https://github.com/norman02/maker-pre-launch-landing-page.git](https://github.com/norman02/maker-pre-launch-landing-page.git)
- Live Site URL: [https://maker-pre-launch-landing-page-tau.vercel.app/](https://maker-pre-launch-landing-page-tau.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS Grid
- Javascript
- Mobile-first workflow
- 7-1 Pattern
- [Sass](https://sass-lang.com/)


### What I learned

I learned a lot about css grid while working on this project. There are several different grid layouts used in this design. I also needed to remember my regular expressiosns RegEx to complete the email validation script:

```js
const isEmail = (email)=> {
    const re = /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
    return re.test(String(email).toLowerCase());
}

const validate = () => {
    const inputEmail = document.getElementById('email').value 
    if (isEmail(inputEmail)) {
        alert(`Email will be sent to ${inputEmail}`)
    } else {
        document.getElementById('cta').classList.toggle('error')
    }
}
```

### Continued development

I would like to continue working on more complex layouts using CSS grid

### Useful resources

- [CSS-Tricks](https://css-tricks.com/) - This helped me with CSS grid as well as formating text areas.

## Author

- Frontend Mentor - [@norman02](https://www.frontendmentor.io/profile/norman02)
- Twitter - [@JohnIsNorman](https://www.twitter.com/JohnIsNorman)

## Acknowledgements

- [Patrick](https://www.frontendmentor.io/profile/palgramming) Thank you for pointing out the bug I had in my transitions.
# Frontend Mentor - Four card feature section solution

This is a solution to the [Four card feature section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/four-card-feature-section-weK1eFYK). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [Some points to explain](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- CSS Grid
- Mobile-first workflow
- SASS

### Some points to explain

In this part I thought of using grid layout to position three sections
of cards: one on the left with one card, one in the middle with two cards and one on the right with one card. This way I could align vertically the side cards in the cells as the height of the row is the same for all cells.
```html
<div class="left">
  <div class="card">
    <h3>Supervisor</h3>
    <p>Monitors activity to identify project roadblocks</p>
    <div class="img">
      <img src="images/icon-supervisor.svg" alt="Supervisor" />
    </div>
  </div>
</div>
<div class="middle">
  <div class="card">
    <h3>Team Builder</h3>
    <p>Scans our talent network to create the optimal team for your project</p>
    <div class="img">
      <img src="images/icon-team-builder.svg" alt="Supervisor" />
    </div>
  </div>
  <div class="card">
    <h3>Karma</h3>
    <p>Regularly evaluates our talent to ensure quality</p>
    <div class="img">
      <img src="images/icon-karma.svg" alt="Supervisor" />
    </div>
  </div>
</div>
<div class="right">
  <div class="card">
    <h3>Calculator</h3>
    <p>Uses data from past projects to provide better delivery estimates</p>
    <div class="img">
      <img src="images/icon-calculator.svg" alt="Supervisor" />
    </div>
  </div>
</div>
```

This is to make the footer take up the remaining space on high devices such as the ipad pro
```css
body {
  font-family: "Poppins", Arial, sans-serif;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  
}
```

Simplest solution I could think of for the cards
```css
@media (min-width: 800px) {
  #cards {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: $gap;
    align-items: center;

    .card {
      max-width: auto;
    }
  }
}
```

This makes the footer grows so as to take up the remaining space and center the paragraph
```css
footer {
  flex: 1 0 auto;
  display: flex;
  align-items: center;
  justify-content: center;
}
```

It sets a limit to the width of the card so that it does not take up the full width
```css
.card {
  max-width: 400px;
}
```

### Useful resources

- [w3docs](https://www.w3docs.com/snippets/html/how-to-make-a-div-fill-the-height-of-the-remaining-space.html) - this helped me figuring out how to make the footer take the remaining spaces on high screens

## Author

- Frontend Mentor - [@rafaeldevvv](https://www.frontendmentor.io/profile/rafaeldevvv)
- Instagram - [@rafffael_maia](https://www.instagram.com/rafffael_maia/)

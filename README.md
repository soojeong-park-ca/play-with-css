# Play with CSS

Play with CSS is a website where you can change the CSS styles(spacing, blur, color) of elements displayed on the website.

## Table of contents

- [Overview](#overview)
  - [Screenshots](#screenshots)
  - [Demo Link](#demo-link)
- [About the Project](#about-the-project)
  - [Status](#status)
  - [Built with](#built-with)
  - [Reflection](#reflection)
- [Author](#author)

## Overview

### Screenshots

Demo video:

https://user-images.githubusercontent.com/126619528/225781858-aeaa8d9a-3a91-4499-966a-dabad2ae57e3.mov

### Demo Link

**[💻 Live Site URL](https://soojeong-park-ca.github.io/play-with-css/)**

## About the Project

### Status

✅ Completed & Deployed

### Built with

- HTML
- CSS
- Vanilla JS

### Reflection

This was another Vanilla JS project from JavaScript 30 course by Wes Bos.

Some features to highlight in this project are:

- using `CSS custom properties` to define the CSS styles on the `:root` so that they can be reused or manipulated in the global scope throughout the whole HTML document.

- using `element.style.setPropery()` method to add inline styles to the selected elements and setting new values to the CSS custom properties.

  ```css
  function changeCSSVal(e) {
    const newVal = `${e.target.value}${
      e.target.dataset.sizing ?
      e.target.dataset.sizing :
      ""
    }`;
    img.style.setProperty(`--${e.target.name}`, newVal);
    highlightedWord.style.setProperty(`--${e.target.name}`, newVal);
  }
  ```

Something new I learned from this project is:

- using the `input` event instead of `change` event to trigger live updates of the changes made to the input elements. 'change' event triggers update only when the mouse is released by the user.

  ```js
  allInputs.forEach(input => {
    input.addEventListener("input", changeCSSVal);
  });
  ```

## Author

Soojeong Park [@codingsooj](https://twitter.com/codingsooj)

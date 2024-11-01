# Navigation Scroll

We want the navigation to change it's style a bit when we scroll because right now, it has a transparent background and it's hard to see the links if we scroll down. So we want to add the `bg-dark` color class to the navigation when we scroll down. We can do this with a little bit of JavaScript.

Open the `js/script.js` file and add the following code:

```js
// User Scroll For Navbar
function userScroll() {
  const navbar = document.querySelector('.navbar');

  window.addEventListener('scroll', () => {
    if (window.scrollY > 50) {
      navbar.classList.add('bg-dark');
    } else {
      navbar.classList.remove('bg-dark');
    }
  });
}

document.addEventListener('DOMContentLoaded', userScroll);
```

What we are doing here is adding an event listener to the window object and listening for the `scroll` event. When the user scrolls, we check if the `window.scrollY` is greater than 50. If it is, we add the `bg-dark` class to the navbar, otherwise we remove it.

## Transition

Right now, this works, but the background just kind of pops into place. We want to add a transition to make it look a little nicer. We can do this by adding the following CSS to the `scss/style.scss` file:

```css
// Navbar
.navbar {
  transition: all 0.5s ease-in-out;
}
```

Now, when we scroll, the background will fade in and out and have a much smoother transition.

We will be doing this with pretty much every project that has a navbar. There may be different styles, but they will all be similar.

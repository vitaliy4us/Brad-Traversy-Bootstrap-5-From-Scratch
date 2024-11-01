# Back To Top Button

The final touch to this page is to add a button that is fixed at the bottom to bring the user back up to the top of the page. This will take a tiny bit of JavaScript. We also want to hide the button until the user scrolls down a bit.

I decided not to use bootstrap for this button because there are styles that bootstrap can not give us such as the position coords and I want to use a different color for the background. I also want this to be completely re-usable on websites that do not use bootstrap.

Let's add the html:

```html
<button id="to-top" class="to-top-btn">
  <img src="images/up-arrow.png" alt="" />
</button>
```

## CSS

Now, the CSS:

```css
/*** Scroll to top button ***/
.to-top-btn {
  position: fixed;
  z-index: 99;
  bottom: 20px;
  right: 20px;
  opacity: 0;
  width: 52px;
  height: 52px;
  border: none;
  border-radius: 50%;
  outline: none;
  background-color: #44434a;
  cursor: pointer;
  transition: all 0.5s ease-in-out;
}

.to-top-btn:hover {
  background-color: #1d1d21;
}

.to-top-btn img {
  margin-bottom: 0.25rem;
  width: 18px;
}

.show {
  opacity: 1;
}
```

We styled the button and also added a show class that will be added to the button when the user scrolls down. This will make the button visible changing the opacity to 1. We also added a transition to make the button fade in and out.

## JavaScript

Since we want this to show when the user starts scrolling, we will do that in the function `userScroll`. Add the following code:

```js
function userScroll() {
  const navbar = document.querySelector('.navbar');
  const toTopBtn = document.querySelector('#to-top'); // add this line

  window.addEventListener('scroll', () => {
    if (window.scrollY > 50) {
      navbar.classList.add('navbar-transparent');
      toTopBtn.classList.add('show'); // add this line
    } else {
      navbar.classList.remove('navbar-transparent');
      toTopBtn.classList.remove('show'); // add this line
    }
  });
}
```

Now, we need the function and event listener to bring the user back up. Add the following code:

```js
function scrollToTop() {
  document.body.scrollTop = 0; // for Safari
  document.documentElement.scrollTop = 0; // for Chrome, Firefox, IE and Opera
}

document.querySelector('#to-top').addEventListener('click', scrollToTop);
```

Now you should have a small button to scroll back up.

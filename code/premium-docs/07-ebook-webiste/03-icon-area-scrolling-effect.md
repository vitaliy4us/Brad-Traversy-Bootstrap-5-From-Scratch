# Icon Area & Scrolling Effect

We have a small area to show some Font Awesome icons and some text. Font awesome should already be included with the simple starter package.

Let's add the following code to the `index.html` file:

```html
<!-- Icon Section -->
<section class="icons bg-light pb-5">
  <div class="container">
    <div class="row">
      <div class="col-md-4 d-flex gap-4">
        <i class="fas fa-user fa-3x text-primary"></i>
        <div>
          <h5 class="fw-bold">Unlock Your Blogging Potential</h5>
          <p class="text-muted">
            Discover the key to unleashing your true blogging potential. Our
            ebook provides expert guidance on creating compelling content
          </p>
        </div>
      </div>
      <div class="col-md-4 d-flex gap-4">
        <i class="fas fa-rocket fa-3x text-secondary"></i>
        <div>
          <h5 class="fw-bold">Skyrocket Your Blog's Success</h5>
          <p class="text-muted">
            Take your blog to new heights with our proven strategies for driving
            traffic and increasing your blog's visibility.
          </p>
        </div>
      </div>
      <div class="col-md-4 d-flex gap-4">
        <i class="fas fa-dollar fa-3x text-primary"></i>
        <div>
          <h5 class="fw-bold">Monetize Your Blog</h5>
          <p class="text-muted">
            Turn your passion for blogging into a profitable venture. Our ebook
            reveals tried-and-tested monetization strategies
          </p>
        </div>
      </div>
    </div>
  </div>
</section>
```

This is pretty simple. We have 3 columns of equal widths. Each column has a Font Awesome icon and some text. We made the icons the primary color and the text the secondary color. We aligned each with flexbox and added a gap of 4.

## Scrolling Effect

Now, we need to add the scrolling effect. Right now, on large screens, our navigation is transparent, which is fine when the menu is at the top, but as we scroll, we want the menu to change to a solid color. We can do this with a little bit of JavaScript.

Open the `js/script.js` file and add the following code:

```js
// User Scroll For Navbar
function userScroll() {
  const navbar = document.querySelector('.navbar');

  window.addEventListener('scroll', () => {
    if (window.scrollY > 50) {
      navbar.classList.add('bg-dark');
      navbar.classList.add('navbar-sticky');
    } else {
      navbar.classList.remove('bg-dark');
      navbar.classList.remove('navbar-sticky');
    }
  });
}

document.addEventListener('DOMContentLoaded', userScroll);
```

What we have here is a function that will fire when the DOM is loaded that will listen for a `scroll` event and if that `scrollY` value is greater than 50, then the class of `bg-dark` and `navbar-sticky` will be added. We know what the `bg-dark` is. It will add a dark background. I also want to add the `navbar-sticky` custom class to add some opacity as well as anything else you want to add.

Open your `scss/style.scss` file and add the following code:

```css
.navbar {
  transition: all 0.5s ease-in-out;
}

.navbar-sticky {
  opacity: 0.9;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
}
```

We are adding opacity and a shadow to the navbar on scroll. I also added a transition on all properties so that the transition is smooth.

Now try scrolling. If there isn't enough content to scroll, just add some dummy content with `lorem1000` and hit `enter`. It will add 1000 dummy text to your page so you can then scroll. Then remove it after.

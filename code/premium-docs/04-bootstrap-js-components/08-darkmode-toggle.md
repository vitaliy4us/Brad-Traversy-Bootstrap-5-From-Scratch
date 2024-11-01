# Darkmode Toggle

We looked at dark mode earlier. In this lesson, I will show you how to toggle between light and dark mode.

In order to have a toggle, you need to add the JavaScript. It is quite long because it also saves the choice in local storage. Here is the Bootstrap documentation page with the JS:

[https://getbootstrap.com/docs/5.3/customize/color-modes/#javascript](https://getbootstrap.com/docs/5.3/customize/color-modes/#javascript)

Link that JS and add the following code to the html:

```html
<!-- Toggle Dark Mode -->
<button
  type="button"
  class="btn btn-dark"
  data-bs-theme-value="dark"
  aria-pressed="true"
>
  Enable Dark Mode
</button>

<button
  type="button"
  class="btn btn-light"
  data-bs-theme-value="light"
  aria-pressed="true"
>
  Enable Light Mode
</button>
```

You should now be able to toggle between light and dark mode.

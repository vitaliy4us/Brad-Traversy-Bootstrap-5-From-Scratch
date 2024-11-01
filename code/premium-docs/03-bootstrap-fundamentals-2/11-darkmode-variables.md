# Dark Mode & CSS Variables

In this lesson, I will show you how to enable dark mode and we will also look at some of the CSS custom properties that Bootstrap uses, in case you want to use them anywhere else.

## Darkmode

Darkmode is a new feature to Bootstrap 5. It is a new class that can be added to the body tag to change the color scheme of the page.

Add the following code and add the `data-bs-theme` attribute to the `html` tag and set it to dark:

```html
<!DOCTYPE html>
<html lang="en" data-bs-theme="dark">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="./assets/css/bootstrap.min.css" />
    <title>Bootstrap Sandbox | Dark Mode</title>
  </head>
  <body>
    <div class="container">
      <h1 class="mb-5">Dark Mode</h1>

      <div class="card" style="width: 18rem">
        <div class="card-header">This is a card</div>
        <div class="card-body">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora,
          voluptas.
        </div>
      </div>
      <!-- Don't go past here -->
    </div>
    <div style="margin-top: 350px"></div>

    <script src="./assets/js/bootstrap.bundle.min.js"></script>
  </body>
</html>
```

Now your page should be dark. If you want an individual element to be light,
you can add the `data-bs-light` attribute to that element.

```html
<div class="card" style="width: 18rem" data-bs-theme="light">
  <div class="card-header">This is a card</div>
  <div class="card-body">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora, voluptas.
  </div>
</div>
```

Later on, I will show you how you can toggle between the two.

## Custom Properties (Variables)

We are not talking about Sass variables here. These are CSS variables. They can be used in your custom CSS.

I am not going to go through all of them. You can find them all at the following link:

[https://getbootstrap.com/docs/5.3/customize/css-variables/](https://getbootstrap.com/docs/5.3/customize/css-variables/)

To give you an example of how to use them. Open a `<style>` tag after the Bootstrap CSS link and add the following code:

```css
body {
  background-color: var(--bs-blue);
}
```

Now you can use that variable anywhere in your CSS.

Again, for a list of all the variables, check out the link above.

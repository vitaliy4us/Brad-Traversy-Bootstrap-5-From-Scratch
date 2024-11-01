# Font Awesome Setup

We will use Font Awesome in just about every project. It's a great source for icons and other UI elements. We could do this multiple ways. The easiest would be to just include the CDN link in our HTML. However, I want you to have a little more control over it and also be able to use it offline. So we will install it with NPM and set it up similar to Bootstrap.

## Install Font Awesome

In your terminal, run the following command:

```bash
npm install @fortawesome/fontawesome-free
```

Create a new file in the `scss` folder called `fontawesome.scss`. This is where we will import Font Awesome and set it up.

If you want, you can look in the `node_modules/@fortawesome/fontawesome-free/scss` folder to see all of the Sass files that we can import.

In the `fontawesome.scss` file, add the following code:

```scss
@import '../node_modules/@fortawesome/fontawesome-free/scss/fontawesome.scss';
@import '../node_modules/@fortawesome/fontawesome-free/scss/brands.scss';
@import '../node_modules/@fortawesome/fontawesome-free/scss/solid.scss';
```

Now, when you run your build or watch command, the Font Awesome CSS will be compiled into the `css` folder.

## Using Font Awesome

Now that we have Font Awesome setup, we can use it in our HTML. Go to the `index.html` file and add the following just above the bootstrap CSS link:

```html
<link rel="stylesheet" href="css/fontawesome.css" />
```

We also need the webfonts. Create a folder called `webfonts` in the `css` folder. Then copy the `webfonts` folder from `node_modules/@fortawesome/fontawesome-free` into the root of the project.

Now in the `index.html` file, add the star icon in the `h1` tag to test it out:

```html
<h1 class="text-primary">
  <i class="fa fa-star"></i> Bootstrap 5 Simple Starter
</h1>
```

If you see the start, you are good to go. We now have our Bootstrap starter package to use with our projects.

# Bootstrap Setup

We now have a workflow to compile our Sass. Next we are going to setup Bootstrap.

Open your terminal and run the following command:

```bash
npm install bootstrap
```

This will install Bootstrap and add it to our `package.json` file.

If you look in the `node_modules` folder, you will see a folder called `bootstrap`. This is where all of the Bootstrap files are. Open the `scss` folder and you will see a file called `_variables.scss`. This is where all of the Bootstrap variables are. We can override these variables in our own Sass files.

We could import all of the bootstrap stuff into the `styles.scss`, but I want to leave that for custom styles. Instead, we will create a new file called `bootstrap.scss` in the `scss` folder. This is where we will import Bootstrap.

Add the following:

```scss
@import '../node_modules/bootstrap/scss/bootstrap';
```

Now when you run the `sass:build` or `sass:watch` script, it will compile Bootstrap into this file.

Run the `sass:build` script and you will see that a `css` folder has been created with a `bootstrap.css` file in it. This is the compiled Bootstrap CSS. Include this in your `index.html` file above your `styles.css` file.

```html
<link rel="stylesheet" href="css/bootstrap.css" />
```

Now you should see the font change and Bootstrap being implemented.

## Customizing Bootstrap

We can override the Bootstrap variables in our own Sass files. Let's change the primary color to red.

Open the `scss/bootstrap.scss` file and add the following above the import:

```scss
$primary: red;
```

Now run either the build script or the watch script.

Add the following to your `index.html` file:

```html
<div
  class="container d-flex flex-column align-items-center justify-content-center text-center vh-100 w-50"
>
  <h1 class="text-primary">Bootstrap 5 Simple Starter</h1>
  <p>
    This is a boilerplate for creating and customizing Bootstrap 5 projects.
  </p>
  <p class="bg-light p-2">
    Look at
    <strong>"node_modules/bootstrap/dist/scss/_variables.scss"</strong> to see
    the variables that you can overwrite in your
    <strong>"bootstrap.scss"</strong> file.
  </p>
</div>
```

Your `text-primary` class should now be red. If you added a `btn-primary` class to a button, it would also be red.

You now have complete customization over the Bootstrap styles and you didn't have to write any custom CSS.

## Bootstrap JavaScript

For the JavaScript, we need to include the `bootstrap.bundle.min.js` file. This includes the Popper.js library that is required for some of the Bootstrap components. You can go into the `node_modules/bootstrap/dist/js` folder and see all of the JavaScript files that are available. Copy the `bootstrap.bundle.min.js` file into your `js` folder.

Then add the following to your `index.html` file right above the ending body tag:

```html
<script src="js/bootstrap.bundle.min.js"></script>
```

We are now ready for Bootstrap development, however there is one more thing that I want to do and that is setup Font Awesome for icons. We can install it with NPM. We will do this in the next lesson.

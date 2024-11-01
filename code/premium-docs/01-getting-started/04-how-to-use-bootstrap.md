# How To Use Bootstrap

Alright, so this video is for the absolute beginners. Many of you probably know this already, but I want to go over the ways that we can use Bootstrap.

## CDN

The first is by using a CDN (Content Delivery Network). Bootstrap provides CDN links that allow you to include the necessary CSS and JavaScript files directly from a remote server. This method is the easiest and quickest way to get started with Bootstrap.

The links will look something like this:

```html
<link
  href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css"
  rel="stylesheet"
  integrity="sha384-9ndCyUaIbzAi2FUVXJi0CjmCapSmO7SnpJef0486qhLnuZ2cdeRhO02iuK6FUUVM"
  crossorigin="anonymous"
/>
<script
  src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"
  integrity="sha384-geWF76RCwLtnZ8qwWowPQNguL3RmwHVBC9FhGdlKrxdiJJigb/j/68SIy3Te4Bkz"
  crossorigin="anonymous"
></script>
```

The latest version of Bootstrap at this time is `5.3` and that is what we will be using.

The link tag is a link to the CSS file. I want to mention that if you use a CDN, you are using the default styles that Bootstrap offers. For instance, when you use a class of `btn-primary`, it will always be the default shade of blue that Bootstrap uses in the primary context. You could write your own CSS that overwrites that color, but that isn't really ideal. If you want to customize, using Sass is a much better way. However, if you just need something quick and you don't really care about customizing, using the CDN is the quickest way.

The script tag is for the JavaScript bundle. This includes all of the javascript needed for the navbar dropdowns, carousels and all that stuff. Bootstrap does have a dependency called Popper.js that it uses for popovers and tooltips. The bundle also includes Popper, so you don't have to manually include it separately like you used to. You used to need that and JQuery, but Bootstrap no longer depends on JQuery.

## Downloading the Files

You can also download the compiled files and include them in your html. This is the same as using a CDN, except your files are local and not remote. Which is good if your client is not connected to the Internet. This is what we'll be using in the JavaScript sandbox. You can download the compiled files at https://getbootstrap.com/docs/5.3/getting-started/download/

## Compiling Source Files Using Sass

The next option is to compile the Sass files. Sass is a style language similar to CSS with some extra features. The Bootstrap Sass files have variables that you can change and then compile a custom version of the Bootstrap CSS files.

You can get the Bootstrap Sass files a few different ways. You can download them at https://getbootstrap.com/docs/5.3/getting-started/download/ or you could install Bootstrap using a package manager like NPM (Node Package Manager), which is what we will be doing for our 5 website projects.

This method may seem a little overwhelming for beginners that have never used Sass or NPM, but I promise you that by the end of this course, you'll see the benefit and you'll be comfortable with these.

Alright, so in the next video, we'll go over what you need to get started, which isn't much at all, but I still want to go over it real quick.

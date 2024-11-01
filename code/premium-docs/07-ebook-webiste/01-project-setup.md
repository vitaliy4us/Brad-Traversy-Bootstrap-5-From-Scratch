# Project Intro & Setup

This is a website for downloading a free E-book called "Blog Mastery". Of course, you could change it to any product that you want. Here are the main features:

- Modern layout with custom colors/styles/backgrounds
- Responsive design
- Sticky navbar with style changes on scroll
- Bootstrap modals
- Form & input styles
- Testimonials
- Contact page with Google Map
- Font Awesome icons

<img src="./images/screen.png" />

# Project Setup

We will be using Sass to compile our CSS. I have included a zip file called `ebook-website-starter`. Download that file, extract it and rename it to `ebook-website`. This will be our starting point for this project.

## What is Included in the Starter?

- The `bs5-simple-starter` files
- The `Open Sans` font from Google Fonts
- Website images
- Website favicon

## Install Dependencies

Open a terminal in the root of the project and run the following command to install the dependencies:

```bash
npm install
```

## Sass

We will need to compile our Sass. Run the following command whenever you are working on the project:

```bash
npm run sass:watch
```

Now you can make changes to the `scss/bootstrap.scss` and `scss/styles.scss` files and they will compile to css.

## Open in Browser

If you are using VS Code, I would suggest using the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension to open the project in your browser. If you are not using VS Code, you can just open the `index.html` file in your browser.

## Bootstrap Variables

In the video course, we will add these when needed and talk about each one, but for the sake of the written tutorials, we will just put all of them in now. Open the `scss/bootstrap.scss` file and add the following to the top of the file:

```scss
// Font
$font-family-sans-serif: 'Open Sans', sans-serif;

// Colors
$primary: #c167ef;
$secondary: #10bcee;
$dark: #2b3041;
$light: #f3f6f9;

// Navbar
$navbar-padding-y: 1rem;
$navbar-dark-color: #fff;
$navbar-dark-hover-color: $secondary;

// Buttons
$button-radius: 50px;
$button-padding-x: 30px;
$button-padding-y: 10px;

$btn-border-radius: $button-radius;
$btn-border-radius-sm: $button-radius;
$btn-border-radius-lg: $button-radius;
$btn-padding-y: $button-padding-y;
$btn-padding-y-lg: $button-padding-y;
$btn-padding-y-sm: $button-padding-y;
$btn-padding-x: $button-padding-x;
$btn-padding-x-lg: $button-padding-x;
$btn-padding-x-sm: $button-padding-x;
$navbar-toggler-border-radius: 5px;

// Spacing
$spacer: 1rem !default;
$spacers: (
  0: 0,
  1: $spacer * 0.25,
  2: $spacer * 0.5,
  3: $spacer,
  4: $spacer * 1.5,
  5: $spacer * 3,
  6: $spacer * 6,
  7: $spacer * 8,
  8: $spacer * 12,
) !default;
$headings-margin-bottom: $spacer * 1;
$line-height-base: 1.7;

$enable-negative-margins: true;

@import '../node_modules/bootstrap/scss/bootstrap';
```

Most of this is pretty self explanatory. We have the main font, colors, navbar, buttons, spacing and container variables. The spacers pertain to the spacing utility classes that Bootstrap provides (eg `my-5`). Usually 5 is the highest number, but we are adding 6, 7 and 8 to give us more options for wider spacing.

The container breakpoints have been changed because I don't want a really wide container and I don't want a huge difference from `lg` to `xxl`. The `enable-negative-margins` variable is set to `true` because we will be using a negative margins class on the image at the bottom that will be outside of the container.

Now that we have our variables set, we can start building our website.

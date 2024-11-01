# Project Intro & Setup

This website is for training courses features that also make it great for online classes, workshops, seminars and coaching sessions. Here are the main features:

- Modern layout with custom colors/styles/backgrounds
- Responsive design
- Sticky navbar with style changes on scroll
- Carousel image slider
- Register & email subscribe forms
- Font Awesome icons

<img src="./images/screen.png" />

# Project Setup

We will be using Sass to compile our CSS. I have included a zip file called `corso-website-starter`. Download that file, extract it and rename it to `corso-website`. This will be our starting point for this project.

## What is Included in the Starter?

- The `bs5-simple-starter` files
- The `Montserrat` font from Google Fonts
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
$font-family-sans-serif: 'Montserrat', sans-serif;

// Colors
$primary: #f8b547;
$secondary: #35353a;
$light: #fbf9f5;
$body-bg: $light;

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

// Navbar
$navbar-nav-link-padding-x: 0.8rem;
$navbar-padding-y: 1rem;
$navbar-dark-color: #fff;

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

$headings-font-weight: bold;

@import '../node_modules/bootstrap/scss/bootstrap';
```

Most of this is pretty self explanatory. We have the main font, colors, navbar, buttons and spacing. The spacers pertain to the spacing utility classes that Bootstrap provides (eg `my-5`). Usually 5 is the highest number, but we are adding 6, 7 and 8 to give us more options for wider spacing.

We also set the headings to have a bold font weight and added more rounded corners to the buttons and navbar toggler.

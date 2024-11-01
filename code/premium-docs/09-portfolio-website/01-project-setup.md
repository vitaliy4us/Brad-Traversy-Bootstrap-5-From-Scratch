# Project Intro & Setup

This is a dark-light contrast website for a portfolio. It is related to being a web developer, but can be edited to be for any type of portfolio. It is a single page website with no navbar. It includes a bit of custom JavaScript for the typewriter effect and uses a script called "Lightbox" for the project modals.

- Dark and light contrast
- Responsive design
- Full height header/hero
- Background image overlays
- Typewriter effect in header
- Lightbox modals for projects
- Progress bar stats
- Font awesome icons

<img src="./images/screen.png" />

# Project Setup

We will be using Sass to compile our CSS. I have included a zip file called `portfolio-website-starter`. Download that file, extract it and rename it to `portfolio-website`. This will be our starting point for this project.

## What is Included in the Starter?

- The `bs5-simple-starter` files
- The `Poppins` and `Lora` fonts from Google Fonts
- Website images
- Website favicon
- Lightbox script

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

If you are using VS Code, I would suggest using the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension to open the project in your browser. If you are not using VS Code, you can just open the `index.html` file in your browser and you should just see the `h1` tag that says "Vera Website".

## Bootstrap Variables

We will be adding some custom variables in the `scss/bootstrap.scss` file. Open that file and add the following to the top of the file:

```scss
// Font
$font-family-sans-serif: 'Poppins', sans-serif;

// Color
$primary: #cc005f;
$secondary: #990047;
$dark: #000;
$light: #f4f4f4;

// Buttons
$button-radius: 0;
$button-padding-x: 30px;
$button-padding-y: 12px;

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

// Container
$container-max-widths: (
  sm: 540px,
  md: 720px,
  lg: 960px,
  xl: 980px,
  xxl: 1000px,
) !default;

@import '../node_modules/bootstrap/scss/bootstrap';
```

We got rid of the rounded corners. We added some extra spacers. The container max widths were changed because I don't want much of a difference between lg and xxl. All 3 sizes will have the same layout.

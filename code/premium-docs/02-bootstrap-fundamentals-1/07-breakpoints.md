# Breakpoints

## What is a CSS breakpoint?

A breakpoint is a point in your CSS where you define a change to the layout of your page. This is usually done to make the page responsive to different screen sizes.

We already talked about this a little bit, but bootstrap has specific breakpoints that you can use to make your page responsive. These are:

- Extra small: <576px
- Small: ≥576px
- Medium: ≥768px
- Large: ≥992px
- Extra large: ≥1200px
- Extra extra large: ≥1400px

The size variations that we can use with specific classes are as follows:

- `xs` - Extra small devices (portrait phones, less than 576px)
- `sm` - Small devices (landscape phones, 576px and up)
- `md` - Medium devices (tablets, 768px and up)
- `lg` - Large devices (desktops, 992px and up)
- `xl` - Extra large devices (large desktops, 1200px and up)

We will get into classes that use these in a bit, but right now, I just want you to be familiar with the breakpoints and how you can target them in your own CSS using media queries.

In your HTML file `head`, add the following CSS:

```html
<style>
  /*  X-Small devices (portrait phones, less than 576px) */
  body {
    background: gray;
  }

  /* `sm` applies to x-small devices (portrait phones, less than 576px) */
  @media (min-width: 576px) {
    body {
      background: red;
    }
  }

  /* `md` applies to small devices (landscape phones, less than 768px) */
  @media (min-width: 767px) {
    body {
      background: blue;
    }
  }

  /* `lg` applies to medium devices (tablets, less than 992px) */
  @media (min-width: 991px) {
    body {
      background: green;
    }
  }

  /* `xl` applies to large devices (desktops, less than 1200px) */
  @media (min-width: 1199px) {
    body {
      background: yellow;
    }
  }

  /* `xxl` applies to x-large devices (large desktops, less than 1400px) */
  @media (min-width: 1399px) {
    body {
      background: purple;
    }
  }
</style>
```

Now change the size of your browser window and see how the background color changes at each breakpoint. These corespond to the classes `sm`, `md`, `lg`, `xl`, and `xxl`.

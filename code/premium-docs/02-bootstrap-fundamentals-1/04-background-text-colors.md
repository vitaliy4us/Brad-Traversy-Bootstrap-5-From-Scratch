# Background & Text Colors

Bootstrap provides a number of utility classes that can be used to change the background and text color of an element as well as its hover state and focus state.

There can be different classes that use the same color. For example, there is a class for the color red, `text-danger`, and a class for the background color red, `bg-danger`. There is also a class for buttons of the color red, `btn-danger`.

The class name variations are as follows:

- \*-primary - blue
- \*-secondary - gray
- \*-success - green
- \*-danger - red
- \*-warning - yellow
- \*-info - light blue
- \*-light - light gray
- \*-dark - dark gray
- \*-white - white
- \*-transparent - transparent

These all have a default color. For example, the default color for `text-primary` is blue. The default color for `bg-primary` is blue. The default color for `btn-primary` is blue.

If you want to change the default color, there are a few ways to do that. You could create your own custom CSS class and override the class/color. I will show you an example of that in a minute. However, if you are going to be changing a lot of default styles, it is better to use Sass, which is a CSS preprocessor. You can actually compile your own version of Bootstrap with your own custom styles. This is what we'll be doing with our main projects. For now, we will stick with the deafult colors.

## Background Colors

Let's look at some classes to change the background color of some elements. I'm using `div` tags, but you could use any element.

```html
<div class="bg-primary">.bg-primary</div>
<div class="bg-secondary">.bg-secondary</div>
<div class="bg-success">.bg-success</div>
<div class="bg-danger">.bg-danger</div>
<div class="bg-warning">.bg-warning</div>
<div class="bg-info">.bg-info</div>
<div class="bg-light">.bg-light</div>
<div class="bg-dark">.bg-dark</div>
<div class="bg-black">.bg-black</div>
<div class="bg-white">.bg-white</div>
<div class="bg-transparent">.bg-transparent</div>
```

## Text Background Colors

Notice some of the text is not readable or would just look better if it were lighter or darker. You have a couple options. You could use a text color class like `text-white` on all of the divs that need it or you could use a text background color class like `text-bg-primary`. Let's use the text background color classes.

```html
<div class="text-bg-primary">.bg-primary</div>
<div class="text-bg-secondary">.bg-secondary</div>
<div class="text-bg-success">.bg-success</div>
<div class="text-bg-danger">.bg-danger</div>
<div class="text-bg-warning">.bg-warning</div>
<div class="text-bg-info">.bg-info</div>
<div class="text-bg-light">.bg-light</div>
<div class="text-bg-dark">.bg-dark</div>
<div class="text-bg-black">.bg-black</div>
<div class="text-bg-white">.bg-white</div>
<div class="text-bg-transparent text-body">.bg-transparent</div>
```

## Text Colors

You can also change the text color of an element. This is useful if you want to change the color of the text inside a button, link, card or anywhere else. Here are the text color classes:

```html
<div class="text-primary">.text-primary</div>
<div class="text-secondary">.text-secondary</div>
<div class="text-success">.text-success</div>
<div class="text-danger">.text-danger</div>
<div class="text-warning">.text-warning</div>
<div class="text-info">.text-info</div>
<div class="text-light bg-dark">.text-light</div>
<div class="text-dark">.text-dark</div>
<div class="text-body">.text-body</div>
<div class="text-muted">.text-muted</div>
<div class="text-black-50">.text-black-50</div>
<div class="text-white-50 bg-dark">.text-white-50</div>
```

## Gradient Backgrounds

To make any of these colors a gradient, simply add the class of `bg-gradient`:

```html
<div class="text-bg-primary bg-gradient">.bg-primary</div>
<div class="text-bg-secondary bg-gradient">.bg-secondary</div>
<div class="text-bg-success bg-gradient">.bg-success</div>
<div class="text-bg-danger bg-gradient">.bg-danger</div>
<div class="text-bg-warning bg-gradient">.bg-warning</div>
<div class="text-bg-info bg-gradient">.bg-info</div>
<div class="text-bg-light bg-gradient">.bg-light</div>
<div class="text-bg-dark bg-gradient">.bg-dark</div>
```

## Background Opacity

You may want the background color to be a little lighter or darker. There are not classes such as `primary-100`, `primary-200`, etc like there is with Tailwind CSS. However, you can use the `opacity-*` classes to make the background color lighter or darker. The opacity classes are as follows:

```html
<div class="text-bg-success p-2">Default success background</div>
<div class="text-bg-success p-2 bg-opacity-75">
  75% opacity success background
</div>
<div class="text-bg-success p-2 bg-opacity-50">
  50% opacity success background
</div>
<div class="bg-success p-2 bg-opacity-25">25% opacity success background</div>
<div class="bg-success p-2 bg-opacity-10">10% opacity success background</div>
```

This will only affect the background color, not the text color or anything inside the element.

There are classes for text opacity as well:

```html
<div class="text-primary">This is default primary text</div>
<div class="text-primary text-opacity-75">This is 75% opacity primary text</div>
<div class="text-primary text-opacity-50">This is 50% opacity primary text</div>
<div class="text-primary text-opacity-25">This is 25% opacity primary text</div>
```

## Link Colors

Links also have color classes:

```html
<p><a href="#" class="link-primary">Primary link</a></p>
<p><a href="#" class="link-secondary">Secondary link</a></p>
<p><a href="#" class="link-success">Success link</a></p>
<p><a href="#" class="link-danger">Danger link</a></p>
<p><a href="#" class="link-warning">Warning link</a></p>
<p><a href="#" class="link-info">Info link</a></p>
```

Like I said, there are other elements where you can use these utility classes, such as buttons and borders. We will look at these in a little bit.

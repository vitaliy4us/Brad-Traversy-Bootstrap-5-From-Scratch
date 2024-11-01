# Typography

Typography is the art and technique of arranging type to make written language legible and appealing. The arrangement of type involves things like selecting typefaces, point sizes, line lengths, line-spacing, letter-spacing and more.

## Font Family

Bootstrap sets basic global display, typography and link styles. It uses a native font stack that selects the best font-family for each operating system and device.

If you open your devtools and select some text, you will see something like the following for the font-stack:

```css
font-family: system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', 'Noto Sans',
  'Liberation Sans', Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol',
  'Noto Color Emoji';
```

Of course, you can change the font-family to whatever you want. You could override it in the CSS, but you can also set a Sass variable if you are compiling Bootstrap from source, which we will be doing later. For now, we will stick with the default stack.

## Headings

There are specific default sizes set to headings.

- h1: 2.5rem
- h2: 2rem
- h3: 1.75rem
- h4: 1.5rem
- h5: 1.25rem
- h6: 1rem

### Relative Units

A rem is a unit of measurement that is relative to the root element. It is similar to em, but em is relative to the parent element. The default font-size is 16px, so 1rem is equal to 16px. 2rem is equal to 32px, because it is twice the size of 1rem.

You can take a look in the devtools to see the default styles for headings.

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

### Heading Classes

You can use classes to change text in any tag to a heading.

```html
<p class="h1">Heading 1 Paragraph</p>
<p class="h2">Heading 2 Paragraph</p>
<p class="h3">Heading 3 Paragraph</p>
<p class="h4">Heading 4 Paragraph</p>
<p class="h5">Heading 5 Paragraph</p>
<p class="h6">Heading 6 Paragraph</p>
```

### Display Headings

There are also display heading classes, which are a larger, slightly more opinionated heading style.

```html
<h1 class="display-1">Display 1</h1>
<h1 class="display-2">Display 2</h1>
<h1 class="display-3">Display 3</h1>
<h1 class="display-4">Display 4</h1>
<h1 class="display-5">Display 5</h1>
<h1 class="display-6">Display 6</h1>
```

## Paragraphs

Here are some classes that you may use in paragraphs.

### Lead

The `.lead` class makes a paragraph stand out by increasing its font size and slightly lightening its color.

```html
<p class="lead">
  Lorem ipsum dolor sit amet consectetur adipisicing elit. Harum dolorum,
  consequuntur aut, ipsam quibusdam rem nostrum maiores asperiores repellendus,
  explicabo itaque. Iure repellat modi possimus fugit consectetur ullam iusto
  autem.
</p>
```

### Inline Elements

There are elements that you can use to emphasize text.

- `<mark>` - highlight text
- `<del>` - strikethrough text
- `<ins>` - underline text
- `<strong>` - bold text
- `<em>` - italic text

```html
<!-- Inline Elements -->
<p>
  Lorem, ipsum dolor sit <mark>This is highlighted text</mark>amet consectetur
  adipisicing <strong>This is strong text</strong>Lorem ipsum dolor sit.
  <del>This is strikethrough text</del> Lorem ipsum dolor sit amet.
  <ins>This is underlined tect</ins> Lorem ipsum dolor sit amet.
  <em>This is italic text</em>
</p>
```

### Inline Classes

Elements should be used for their semantic meaning, but you can also use classes to change the appearance of text.

```html
<p>
  Lorem, ipsum dolor sit
  <span class="mark">This is highlighted text</span>amet consectetur adipisicing
  <span class="strong">This is strong text</span>Lorem ipsum dolor sit.
  <span class="del">This is strikethrough text</span> Lorem ipsum dolor sit
  amet. <span class="ins">This is underlined tect</span> Lorem ipsum dolor sit
  amet. <span class="em">This is italic text</span>
</p>
```

### Blockquote

There is also a `blockquote` class that you can use to style a blockquote.

```html
<blockquote class="blockquote">
  <p>This is a blockquote</p>
</blockquote>
```

## Text Utilities

There are a bunch of classes to change the appearance of text. Let's take a look at some of them.

### Font Weight

There are classes for different weights of fonts.

```html
<p class="fw-bold">This is bold text</p>
<p class="fw-bolder">This is bolder text (relative to the parent element).</p>
<p class="fw-semibold">This is semibold text</p>
<p class="fw-medium">This is a medium weight</p>
<p class="fw-normal">This is a normal weight</p>
<p class="fw-light">This is light weight text</p>
<p class="fw-lighter">
  This is lighter weight text (relative to the parent element).
</p>
<p class="fst-italic">This is italic text.</p>
<p class="fst-normal">This is text with normal font style</p>
```

## Line Height

Line height is the vertical space between lines of text. The default line height is 1.5, but there are classes to change it.

```html
<p class="lh-1">
  Lorem ipsum dolor sit amet consectetur adipisicing elit. Itaque dolor sit
  obcaecati architecto necessitatibus velit? Excepturi culpa ipsa enim eveniet,
  alias assumenda quas omnis laborum atque ipsam ipsum minima a.
</p>
<p class="lh-sm">
  Lorem ipsum dolor sit amet consectetur adipisicing elit. Itaque dolor sit
  obcaecati architecto necessitatibus velit? Excepturi culpa ipsa enim eveniet,
  alias assumenda quas omnis laborum atque ipsam ipsum minima a.
</p>
<p class="lh-base">
  Lorem ipsum dolor sit amet consectetur adipisicing elit. Itaque dolor sit
  obcaecati architecto necessitatibus velit? Excepturi culpa ipsa enim eveniet,
  alias assumenda quas omnis laborum atque ipsam ipsum minima a.
</p>
<p class="lh-lg">
  Lorem ipsum dolor sit amet consectetur adipisicing elit. Itaque dolor sit
  obcaecati architecto necessitatibus velit? Excepturi culpa ipsa enim eveniet,
  alias assumenda quas omnis laborum atque ipsam ipsum minima a.
</p>
```

### Text Transform

We have classes to change the case of text.

```html
<p class="text-lowercase">lowercased text</p>
<p class="text-uppercase">uppercased text</p>
<p class="text-capitalize">capitialized text</p>
```

### Text Alignment

We have classes to align the text. There are also responsive classes that will change the alignment based on the screen size.

```html
<p class="text-lowercase">lowercased text</p>
<p class="text-uppercase">uppercased text</p>
<p class="text-capitalize">capitialized text</p>

<!-- Text Alignment -->
<p class="text-start">Start aligned text on all viewport sizes.</p>
<p class="text-center">Center aligned text on all viewport sizes.</p>
<p class="text-end">End aligned text on all viewport sizes.</p>

<p class="text-sm-start">
  Start aligned text on viewports sized SM (small) or wider.
</p>
<p class="text-md-start">
  Start aligned text on viewports sized MD (medium) or wider.
</p>
<p class="text-lg-start">
  Start aligned text on viewports sized LG (large) or wider.
</p>
<p class="text-xl-start">
  Start aligned text on viewports sized XL (extra-large) or wider.
</p>
```

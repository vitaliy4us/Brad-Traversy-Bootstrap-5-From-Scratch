# Cards

Cards are a flexible and extensible content container. It includes options for headers and footers, a wide variety of content, contextual background colors, and powerful display options.

## Basic Text Card

Let's look at a very basic example of a card with some text. I am also going to add a width so that it is not as wide as the screen. Typically, you will put multiple cards next to each other.

```html
<div class="card w-50">
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <p class="card-text">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestias nihil
      harum consequuntur labore! Laudantium veritatis deleniti dolores facilis
      hic placeat.
    </p>
  </div>
</div>
```

As you can see, in addition to the `card` class, we have a `card-body` and an optional `card-title` and `card-text` class. If you do not use the `card-body` class, it will not have any padding.

## Card with Image

We can include an image in our card. I will also add a button.

```html
<div class="card" style="width: 20rem">
  <img src="https://picsum.photos/200" class="card-img-top" alt="..." />
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <p class="card-text">
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nostrum alias
    </p>
    <a href="#" class="btn btn-primary">Read More</a>
  </div>
</div>
```

## Card Header and Footer

We can also add a header and a footer:

```html
<div class="card" style="width: 20rem">
  <div class="card-header">Card Header</div>
  <div class="card-body">
    <h5 class="card-title">Card Title</h5>
    <p class="card-text">
      With supporting text below as a natural lead-in to additional content.
    </p>
    <a href="#" class="btn btn-primary">Read More</a>
  </div>
  <div class="card-footer">Card Footer</div>
</div>
```

## List Group Card

We can contain a list group in a card:

```html
<div class="card" style="width: 20rem">
  <ul class="list-group list-group-flush">
    <li class="list-group-item">Item One</li>
    <li class="list-group-item">Item Two</li>
    <li class="list-group-item">Item Three</li>
  </ul>
</div>
```

## Horizontal Card

We can create an image card with the image on the side instead of the top:

```html
<div class="card mb-3" style="max-width: 540px">
  <div class="row g-0">
    <div class="col-md-4">
      <img
        src="https://picsum.photos/200"
        class="img-fluid rounded-start"
        alt="..."
      />
    </div>
    <div class="col-md-8">
      <div class="card-body">
        <h5 class="card-title">Card title</h5>
        <p class="card-text">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Itaque
          aliquam laudantium aspernatur nesciunt molestiae maiores.
        </p>
        <p class="card-text">
          <small class="text-body-secondary">Last updated 5 mins ago</small>
        </p>
      </div>
    </div>
  </div>
</div>
```

## Grid Columns & Colors

In many cases, you will put your cards in a grid. We are going to use the grid classes to create a four column grid with cards that have different colors. We can use the `bg` or `text-bg-` classes to change the background color of the card.

```html
<div class="row">
  <div class="col-md-3">
    <div class="card text-bg-primary mb-3">
      <div class="card-header">Header</div>
      <div class="card-body">
        <h5 class="card-title">Primary</h5>
        <p class="card-text">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit.
          Exercitationem illo tempore sunt nemo possimus aut.
        </p>
      </div>
    </div>
  </div>
  <div class="col-md-3">
    <div class="card text-bg-secondary mb-3">
      <div class="card-header">Header</div>
      <div class="card-body">
        <h5 class="card-title">Secondary</h5>
        <p class="card-text">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit.
          Exercitationem illo tempore sunt nemo possimus aut.
        </p>
      </div>
    </div>
  </div>
  <div class="col-md-3">
    <div class="card text-bg-success mb-3">
      <div class="card-header">Header</div>
      <div class="card-body">
        <h5 class="card-title">Success</h5>
        <p class="card-text">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit.
          Exercitationem illo tempore sunt nemo possimus aut.
        </p>
      </div>
    </div>
  </div>
  <div class="col-md-3">
    <div class="card text-bg-danger mb-3">
      <div class="card-header">Header</div>
      <div class="card-body">
        <h5 class="card-title">Danger</h5>
        <p class="card-text">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit.
          Exercitationem illo tempore sunt nemo possimus aut.
        </p>
      </div>
    </div>
  </div>
</div>
```

## Card Groups

In addition to the grid, we can also use card groups. This will give us a nice border around the cards.

```html
<div class="card-group">
  <div class="card">
    <img src="https://picsum.photos/200" class="card-img-top" alt="" />
    <div class="card-body">
      <h5 class="card-title">Card title</h5>
      <p class="card-text">
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Iusto soluta
        aliquam odio quam quidem. Odio neque vel exercitationem voluptatibus
        voluptas.
      </p>
    </div>
  </div>
  <div class="card">
    <img src="https://picsum.photos/300" class="card-img-top" alt="" />
    <div class="card-body">
      <h5 class="card-title">Card title</h5>
      <p class="card-text">
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Iusto soluta
        aliquam odio quam quidem. Odio neque vel exercitationem voluptatibus
        voluptas.
      </p>
    </div>
  </div>
  <div class="card">
    <img src="https://picsum.photos/400" class="card-img-top" alt="" />
    <div class="card-body">
      <h5 class="card-title">Card title</h5>
      <p class="card-text">
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Iusto soluta
        aliquam odio quam quidem. Odio neque vel exercitationem voluptatibus
        voluptas.
      </p>
    </div>
  </div>
</div>
```

## Placeholders

The last thing that I want to show you are placeholders. These are basically used to display while your content is loading. It's a bit more creative than just showing a spinner.

Let's say the card that is going to show has a heading and a few lines of text in the body. So you could add the following when the page is loading:

```html
<!-- Placeholders -->
<div class="card" style="width: 18rem" aria-hidden="true">
  <div class="card-body">
    <h5 class="card-title placeholder-glow">
      <span class="placeholder col-6"></span>
    </h5>
    <p class="card-text placeholder-glow">
      <span class="placeholder col-7"></span>
      <span class="placeholder col-4"></span>
      <span class="placeholder col-4"></span>
      <span class="placeholder col-6"></span>
      <span class="placeholder col-8"></span>
    </p>
    <a class="btn btn-primary disabled placeholder col-6"></a>
  </div>
</div>
```

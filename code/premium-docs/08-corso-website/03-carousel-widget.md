# Carousel Widget

We created the header in the last lesson, now we want to add the carousel widget.

Open the `index.html` file and add the following code under the comment `<!-- Image Slider -->`:

```html
<div
  id="carouselExampleIndicators"
  class="carousel slide"
  data-bs-ride="carousel"
>
  <div class="carousel-indicators">
    <button
      type="button"
      data-bs-target="#carouselExampleIndicators"
      data-bs-slide-to="0"
      class="active"
      aria-current="true"
      aria-label="Slide 1"
    ></button>
    <button
      type="button"
      data-bs-target="#carouselExampleIndicators"
      data-bs-slide-to="1"
      aria-label="Slide 2"
    ></button>
    <button
      type="button"
      data-bs-target="#carouselExampleIndicators"
      data-bs-slide-to="2"
      aria-label="Slide 3"
    ></button>
  </div>
  <div class="carousel-inner rounded-5">
    <div class="carousel-item active">
      <img
        src="./images/header-slide-1.jpg"
        class="d-block w-100 rounded-5"
        alt=""
      />
    </div>
    <div class="carousel-item">
      <img
        src="./images/header-slide-2.jpg"
        class="d-block w-100 rounded-5"
        alt=""
      />
    </div>
    <div class="carousel-item">
      <img
        src="./images/header-slide-3.jpg"
        class="d-block w-100 rounded-5"
        alt=""
      />
    </div>
  </div>
  <button
    class="carousel-control-prev"
    type="button"
    data-bs-target="#carouselExampleIndicators"
    data-bs-slide="prev"
  >
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Previous</span>
  </button>
  <button
    class="carousel-control-next"
    type="button"
    data-bs-target="#carouselExampleIndicators"
    data-bs-slide="next"
  >
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Next</span>
  </button>
</div>
```

This is a pretty standard Bootstrap carousel. We have three slides, each with an image. The images are stored in the `images` folder. We also added the indicators and the controls.

### Sizing the Carousel

I want the carousel to be a little more narrow, so I am going to change the width to 90%. Open the `scss/styles.scss` file and add the following code:

```scss
.header .slide {
  width: 90%;
  margin: 0 auto;
}
```

This makes it a bit smaller and centers it on the page.

### Header Height on Small Screens

On small screens, you may notice that the header is too tall and there is a lot of empty space, even with the carousel. Let's change the min-height and height in a `@media` query. Add the following code to the `scss/styles.scss` file:

```scss
@media (max-width: 992px) {
  // ...

  .header {
    height: 800px !important;
    min-height: 800px !important;
  }
}
```

With the slider, it should look like this:

<img src="./images/slider.png" />

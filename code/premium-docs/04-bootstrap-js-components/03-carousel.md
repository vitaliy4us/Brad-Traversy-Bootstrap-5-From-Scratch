# Carousel

A carousel is a slideshow for cycling through a series of images. Let's crete simple carousel of images.

```html
<div id="slider" class="carousel slide">
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img
        src="https://kajabi-storefronts-production.kajabi-cdn.com/kajabi-storefronts-production/file-uploads/themes/2152537062/settings_images/18b2741-a50-55da-37bc-c77252583e_modernjs.webp"
        class="d-block w-100"
        alt="..."
      />
    </div>
    <div class="carousel-item">
      <img
        src="https://kajabi-storefronts-production.kajabi-cdn.com/kajabi-storefronts-production/file-uploads/themes/2152537062/settings_images/a6146c8-c550-e60d-83d-da0202f6bd7_258ea558-245b-4906-b8d6-3412e8d6f0a7.jpg"
        class="d-block w-100"
        alt="..."
      />
    </div>
    <div class="carousel-item">
      <img
        src="https://kajabi-storefronts-production.kajabi-cdn.com/kajabi-storefronts-production/file-uploads/themes/2152537062/settings_images/825ccb4-0ffc-3c0f-8f8e-4f043c0027_2ce67a0-d43b-28cb-bc33-e0acb621bde_Tailwind_CSS_Course.webp"
        class="d-block w-100"
        alt="..."
      />
    </div>
  </div>
  <button
    class="carousel-control-prev"
    type="button"
    data-bs-target="#slider"
    data-bs-slide="prev"
  >
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Previous</span>
  </button>
  <button
    class="carousel-control-next"
    type="button"
    data-bs-target="#slider"
    data-bs-slide="next"
  >
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Next</span>
  </button>
</div>
```

We start with a container div with the class of `carousel`. I also gave it an id of `slider`. Inside that we have a div with the class of `carousel-inner`. Inside that we have a series of divs with the class of `carousel-item`. Each of these divs contains an image. I used my course images, but you could use anything.

At the bottom we have two buttons. One with the class of `carousel-control-prev` and one with the class of `carousel-control-next`. These are the buttons that will allow us to go to the previous and next slide. They both have a `data-bs-target` attribute that points to the id of the carousel. They also both have a `data-bs-slide` attribute that tells it to slide to the previous or next slide.

## Indicators

You can add indicators by adding the following html right under the first `div`:

```html
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
```

## Captions

You can add captions by putting the following right under the image tag:

```html
<div class="carousel-caption d-none d-md-block">
  <h5>First slide label</h5>
  <p>Some representative placeholder content for the first slide.</p>
</div>
```

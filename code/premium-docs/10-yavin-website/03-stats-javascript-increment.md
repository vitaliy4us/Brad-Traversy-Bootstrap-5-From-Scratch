# Stats & JavaScript Increment

In this lesson, we will create the stats with and increment animation. We will also create the introduction and details sections.

## Stats

We will be using some custom JavaScript from one of the projects in my [50 Projects in 50 Days](https://www.traversymedia.com/50-Projects-In-50-Days) course.

Let's add the following to the `index.html` file:

```html
<!-- Stats -->
<section id="stats" class="stats container">
  <div class="row my-6">
    <div class="col-md-3 col-sm-6 text-center">
      <h2 class="counter xl-text" data-target="328"></h2>
      <p>Happy Customers</p>
    </div>
    <div class="col-md-3 col-sm-6 text-center">
      <h2 class="counter xl-text" data-target="285"></h2>
      <p>Issues Solved</p>
    </div>
    <div class="col-md-3 col-sm-6 text-center">
      <h2 class="counter xl-text" data-target="159"></h2>
      <p>Good Reviews</p>
    </div>
    <div class="col-md-3 col-sm-6 text-center">
      <h2 class="counter xl-text" data-target="128"></h2>
      <p>Case Studies</p>
    </div>
  </div>
</section>
```

We are using the `counter` class for the stats and using the `xl-text` class to make the text really large. We are also using the `data-target` attribute to set the target number for the counter. We will be using this in the JavaScript.

They will be 4 across on larger screens and 2 across on smaller screens and stacked on mobile.

## The JavaScript

Create a file called `script.js` in the `js` folder. Add the following to the file:

```js
function incrementStats() {
  const counters = document.querySelectorAll('.counter');

  counters.forEach((counter) => {
    counter.innerText = '0';

    const updateCounter = () => {
      const target = +counter.getAttribute('data-target');
      const c = +counter.innerText;

      const increment = target / 200;

      if (c < target) {
        counter.innerText = `${Math.ceil(c + increment)}`;
        setTimeout(updateCounter, 1);
      } else {
        counter.innerText = target;
      }
    };

    updateCounter();
  });
}

document.addEventListener('DOMContentLoaded', incrementStats);
```

It should look like this:

<img src="./images/yavin3.png" />


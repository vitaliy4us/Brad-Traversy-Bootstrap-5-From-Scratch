# Accordion & Collapse

We are going to look at two JavaScript driven components in this lesson, the accordion and the collapse. The accordion is a series of collapsible items that can be toggled open and closed. The collapse component is a single item that can be toggled open and closed.

## Accordion

Let's create a simple accordion:

```html
<div class="accordion" id="myaccordion">
  <div class="accordion-item">
    <h2 class="accordion-header">
      <button
        class="accordion-button"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#collapseOne"
        aria-expanded="true"
        aria-controls="collapseOne"
      >
        Accordion Item 1
      </button>
    </h2>
    <div
      id="collapseOne"
      class="accordion-collapse collapse show"
      data-bs-parent="#myaccordion"
    >
      <div class="accordion-body">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Placeat animi
        possimus doloribus, magnam ullam deserunt earum iusto doloremque
        incidunt. Minus asperiores quas voluptatibus amet? Non nobis deserunt
        quia rerum facilis tenetur, amet laboriosam sed illo ad? Odio natus ab
        delectus?
      </div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header">
      <button
        class="accordion-button collapsed"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#collapseTwo"
        aria-expanded="false"
        aria-controls="collapseTwo"
      >
        Accordion Item 2
      </button>
    </h2>
    <div
      id="collapseTwo"
      class="accordion-collapse collapse"
      data-bs-parent="#myaccordion"
    >
      <div class="accordion-body">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit totam
        iusto magnam illum, pariatur quia maxime quas obcaecati porro commodi.
        Beatae, similique quisquam vel aliquid hic ratione, consequuntur iusto
        sunt rem accusamus excepturi quos pariatur rerum reprehenderit
        asperiores enim alias.
      </div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header">
      <button
        class="accordion-button collapsed"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#collapseThree"
        aria-expanded="false"
        aria-controls="collapseThree"
      >
        Accordion Item 3
      </button>
    </h2>
    <div
      id="collapseThree"
      class="accordion-collapse collapse"
      data-bs-parent="#myaccordion"
    >
      <div class="accordion-body">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Facilis cum
        odio blanditiis, consectetur ab labore corporis doloribus possimus id
        fugiat rerum reiciendis. Perspiciatis animi voluptatibus expedita sunt
        vitae ea obcaecati!
      </div>
    </div>
  </div>
</div>
```

We start with a container with the class of `accordion`. Inside that we have a series of `accordion-item` divs. Inside each of those we have an `accordion-header` and an `accordion-body`. The header contains a button with the class of `accordion-button`. This button has a few attributes that are important:

- `data-bs-toggle="collapse"` - This tells Bootstrap that this button will toggle the collapse of the accordion item.
- `data-bs-target="#collapseOne"` - This tells Bootstrap which item to collapse. The value is the id of the accordion item.
- `aria-expanded="true"` - This tells screen readers that the accordion item is expanded.
- `aria-controls="collapseOne"` - This tells screen readers that the accordion item is controlled by the element with the id of `collapseOne`.

The accordion item also has a class of `show` which tells Bootstrap to show the item by default.

The second accordion item has a class of `collapsed` which tells Bootstrap to collapse the item by default.

The accordion item also has a `data-bs-parent` attribute which tells Bootstrap that the accordion item is controlled by the element with the id of `myaccordion`.

## Collapse

The collapse component is a single item that can be toggled open and closed. It is very similar to the accordion item.

```html
<div class="my-3">
  <button
    class="btn btn-primary"
    type="button"
    data-bs-toggle="collapse"
    data-bs-target="#mycontent"
    aria-expanded="false"
    aria-controls="mycontent"
  >
    Toggle Content
  </button>
</div>
<div class="collapse" id="mycontent">
  <div class="card card-body">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Non, nam asperiores
    quasi unde laudantium incidunt, accusantium laboriosam eos illo aspernatur
    sed expedita maiores nostrum earum ea velit quidem repudiandae quis!
  </div>
</div>
```

We used a button, but this could just as well be a link. The button has a few attributes that are important:

- `data-bs-toggle="collapse"` - This tells Bootstrap that this button will toggle the collapse of the item.
- `data-bs-target="#mycontent"` - This tells Bootstrap which item to collapse. The value is the id of the collapse item.
- `aria-expanded="false"` - This tells screen readers that the collapse item is collapsed.
- `aria-controls="mycontent"` - This tells screen readers that the collapse item is controlled by the element with the id of `mycontent`.

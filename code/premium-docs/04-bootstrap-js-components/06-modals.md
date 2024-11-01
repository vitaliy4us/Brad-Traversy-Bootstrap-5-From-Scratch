# Modals

Modals are one of the most convienient JavaScript components that bootstrap provides. They are a great way to display information to the user without having to create a new page. Let's create a modal:

```html
<!-- Modal -->
<div
  class="modal fade"
  id="myModal"
  tabindex="-1"
  aria-labelledby="myModalLabel"
  aria-hidden="true"
>
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h1 class="modal-title fs-5" id="myModalLabel">Modal title</h1>
        <button
          type="button"
          class="btn-close"
          data-bs-dismiss="modal"
          aria-label="Close"
        ></button>
      </div>
      <div class="modal-body">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Perferendis
        ratione consequatur iure inventore repellat nisi est voluptatum quae
        quidem tempora optio aut quam laborum, expedita alias sit incidunt
        corrupti unde.
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">
          Close
        </button>
        <button type="button" class="btn btn-primary">Save changes</button>
      </div>
    </div>
  </div>
</div>
```

There are quite a few classes that go into a modal. Let's break them down:

- `modal` - This is the main class that tells Bootstrap that this is a modal.
- `fade` - This tells Bootstrap that the modal should fade in and out.
- `modal-dialog` - This is the container for the modal.
- `modal-content` - This is the content of the modal.
- `modal-header` - This is the header of the modal.
- `modal-title` - This is the title of the modal.
- `modal-body` - This is the body of the modal.
- `modal-footer` - This is the footer of the modal.

We also have some `aria` attributes. These are for accessibility. The `aria-labelledby` attribute tells screen readers that the modal has a title. The `aria-hidden` attribute tells screen readers that the modal is hidden.

We also have a close button. This is a button that will close the modal. It has the `data-bs-dismiss` attribute. This tells Bootstrap that this button should close the modal.

Nothing is actually going to show here yet. We need to trigger the modal. Let's add a button to do that:

```html
<button
  type="button"
  class="btn btn-primary"
  data-bs-toggle="modal"
  data-bs-target="#myModal"
>
  Open Modal
</button>
```

The button has the `data-bs-toggle` attribute. This tells Bootstrap that this button should toggle a modal. The `data-bs-target` attribute tells Bootstrap which modal to toggle.

## Static Backdrop

By default, the modal will close when you click outside of it. You can disable this by adding the `data-bs-backdrop="static"` attribute to the modal.

## Center Vertically

If you want the modal cenetered vertically on the page, you can add the `modal-dialog-centered` class to the `modal-dialog` element.

## Sizing

There are different sizes as well:

- `modal-sm` - Small
- `modal-lg` - Large
- `modal-xl` - Extra Large

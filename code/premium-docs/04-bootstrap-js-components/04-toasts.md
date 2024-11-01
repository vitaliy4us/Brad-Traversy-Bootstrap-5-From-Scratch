# Toasts

Toasts are lightweight notifications designed to mimic the push notifications that have been popularized by mobile and desktop operating systems. They’re built with flexbox, so they’re easy to align and position.

If you want to show a toast at a certain point, you will need to specify in your JavaScript when to show it. You can do this by using the `show()` method on the toast element. It should hide itself after a few seconds, but you can also hide it manually by using the `hide()` method.

Let's add the html for the toast:

```html
<button type="button" class="btn btn-primary" id="toastBtn">
  Show Toast
</button>

<div class="toast-container position-fixed bottom-0 end-0 p-3">
  <div class="toast" id="myToast" role="alert">
    <div class="toast-header text-bg-danger">
      <div class="me-auto">Bootstrap</div>
      <small>11 mins ago</small>
      <button class="btn-close" data-bs-dismiss="toast"></button>
    </div>
    <div class="toast-body text-bg-danger">
      Hello World! This is a toast message
    </div>
  </div>
</div>
```

We have a button to trigger it, but in reality you would probably want to trigger on something like a form submission. We have a container div with the class of `toast-container`. Inside that we have a div with the id of `liveToast` and the class of `toast`. Inside that we have a div with the class of `toast-header` and a div with the class of `toast-body`.

You can style it however you want. Showing an error is a common use of toasts, so I made it red with the class of `text-bg-danger`.

This will not work yet, we need to trigger it on the button click from within JavaScript. Let's do that now. Put a `script` tag at the bottom of the body and add the following code:

```js
const toastTrigger = document.getElementById('toastBtn');
const toast = document.getElementById('myToast');

if (toastTrigger) {
  const toastBootstrap = bootstrap.Toast.getOrCreateInstance(toast);
  toastTrigger.addEventListener('click', () => {
    toastBootstrap.show();
  });
}
```

We get the button and the toast element. We then check if the button exists. If it does, we create a new instance of the toast and add an event listener to the button. When the button is clicked, we show the toast.

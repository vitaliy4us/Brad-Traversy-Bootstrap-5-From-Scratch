# Form Validation Display

Bootstrap has classes to help us display validation messages. Let's create a form with a few fields and we will add some messages for good feedback and invalid feedback. We are also going to add `novalidate` to the form tag so that we don't see the browser's default validation messages.

```html
<form novalidate>
  <div class="mb-3">
    <label for="username" class="form-label">Username</label>
    <input type="text" class="form-control" id="username" required />
    <div class="valid-feedback">Looks Good</div>
    <div class="invalid-feedback">Please choose a username.</div>
  </div>
  <div class="mb-3">
    <label for="email" class="form-label">Email address</label>
    <input type="email" class="form-control" id="email" required />
    <div class="valid-feedback">Looks Good</div>

    <div class="invalid-feedback">Please provide a valid email</div>
  </div>
  <div class="mb-3">
    <label for="city" class="form-label">City</label>
    <input type="text" class="form-control" id="city" required />
    <div class="valid-feedback">Looks Good</div>

    <div class="invalid-feedback">Please provide a valid city.</div>
  </div>

  <div class="mb-3">
    <div class="form-check">
      <input
        class="form-check-input"
        type="checkbox"
        value=""
        id="invalidCheck"
        required
      />
      <label class="form-check-label" for="invalidCheck">
        Agree to terms and conditions
      </label>
      <div class="invalid-feedback">You must agree before submitting.</div>
    </div>
  </div>

  <input type="submit" class="btn btn-primary" value="Submit" />
</form>
``` 

So what we have done is added a message if the field is currently valid and
if it is invalid, however we don't see these messages, even when submitting the
form. These classes will only work if the `form` tag has the `was-validated`
class. Let's add that manually: 

```html
<form novalidate class="was-validated">
``` 

Now you should see a red outline around the fields that are invalid and
  the messages should be displayed. Start to type in the username field and you
  will see the message change to "Looks Good" and the outline will turn green.
  So Bootstrap gives us this dynamic feedback based on the state of the field.
  If the field is valid, it will show the valid feedback message and if it is
  invalid, it will show the invalid feedback message. Obviously, we want this
  stuff to be displayed when the user submits the form, not just when they start
  typing. So let's remove the `was-validated` class and add a class of
  `needs-validation`. Then we will add some custom JavaScript to add the
  `was-validated` class when the form is submitted. 

```js
  <script>
    (() => {
      'use strict';

      // Fetch all the forms we want to apply custom Bootstrap validation styles to
      const forms = document.querySelectorAll('.needs-validation');

      // Loop over them and prevent submission
      Array.from(forms).forEach((form) => {
        form.addEventListener(
          'submit',
          (event) => {
            if (!form.checkValidity()) {
              event.preventDefault();
              event.stopPropagation();
            }

            form.classList.add('was-validated');
          },
          false
        );
      });
    })();
  </script>
</form>
```

What we are doing here is selecting all the forms that have the class of `needs-validation` and then we are looping over them and adding an event listener for the submit event. When the form is submitted, we are checking to see if the form is valid. If it is not valid, we are preventing the default behavior and stopping the event from bubbling up. Then we are adding the `was-validated` class to the form. Now when you submit the form, you will see the validation messages and the red outline around the invalid fields. If you fix the invalid fields, the green outline will appear and the message will change to "Looks Good".

So now you can just run this and add dynamic validation to your forms. You can also use the `:valid` and `:invalid` pseudo classes to style the fields based on their state.

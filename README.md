jQuery Validate Error Message Attribute Extension
========================

Extension to add [jquery validate](http://jqueryvalidation.org/) error messages as a data attribute of elements and helps with localization.  I found it annoying to try to add error messages in javascript on a large website with many forms, so instead I created this extension that makes it an attribute of the input/select/textarea you want to validate.

You have to include both javascript files (jquery.validate before the extension) like so:

```html
<script src="//cdnjs.cloudflare.com/ajax/libs/jquery-validate/1.11.1/jquery.validate.min.js"></script>
<script src="jquery.validate.error.js"></script>
```

Then after, add the `data-error-msg` attribute on your inputs/selects/textareas to add a custom error message.  This works exactly like using the [error message javascript object](http://jqueryvalidation.org/validate/) with validate, but the attribute has higher priority than the javascript version.  Then make sure that your form is validated by doing `$('form').validate();`.

```html
<input type="text" name="name" required data-error-msg="Please enter your name">
```
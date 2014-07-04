bootstrap3-contact-form
=======================

Bootstrap 3 Contact Form with Captcha

A simple bootstrap 3 contact form using [SecureImage Captcha](https://github.com/dapphp/securimage).

### Current Version
Bumps bootstrap version to 3.1.1 and adds optional fields of Title, Company, and Website, along with Phone field.

### Version 1.0
A simpler version of the contact form without the optional fields outlined above: [V 1.0](https://github.com/jonmbake/bootstrap3-contact-form/tree/v1.0).

## Dependencies

* [Bootstrap 3](https://github.com/twbs/bootstrap) version >3.1
* PHP (version > 5.2.0) installed on your server **Must have gd library enabled**
* [SecureImage Captcha](https://github.com/dapphp/securimage) Captcha (included in [library/vender/securimage/**](https://github.com/jonmbake/bootstrap3-contact-form/tree/master/library/vender/securimage))
* jQuery
* **The HTML for the contact form**, which can be extracted from index.html
* **Optional** [International Telephone Input](https://github.com/Bluefieldscom/intl-tel-input) (included in [assets/vender/intl-tel-input/**](https://github.com/jonmbake/bootstrap3-contact-form/tree/master/assets/vender/intl-tel-input))- This is used to validate and format the phone input field. Only need this if the phone field is present.

### Adding or Removing Fields
To add or remove a field from the contact form:

1. Add or remove the HTML element from the form (the *form-group*)
2. When adding, if the field is optional then add the class `.optional` to the input in the element
3. Add or remove an entry from the `$fields_req` array (map) in *sendmail.php* (if the field is required the map entry's value must be true, otherwise false)

### Further Configuration
* **Required** Change the MY_EMAIL constant in library/sendmail.php to the email address you want the contant form data to get submitted to.  You can also change the email subject by editing EMAIL_SUBJECT.
* By default required field inputs are appended with an asterisk.  If you want to remove this feature, add the class `.no-asterisk` to the required input of the form group.

## Check It Out
Demo: http://jonbake.com/demos/contact-form/

Blog Post: http://jonbake.com/blog/?p=115

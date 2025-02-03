# JS Captcha

`Google Captcha`
```html
<!-- GOOGLE CAPTCHA -->
<script src="https://www.google.com/recaptcha/api.js" async defer></script>
<div class="g-recaptcha" data-sitekey="YOUR_SITE_KEY"></div>

<script>
document.addEventListener("DOMContentLoaded", function () {
  const form = document.getElementById("YOUR_FORM_ID");
  if (!form) return;
  
  form.addEventListener("submit", function (event) {
    const recaptchaResponse = grecaptcha.getResponse();
    if (!recaptchaResponse) {
      event.preventDefault(); // Stop form submission
      alert("Please complete the CAPTCHA before submitting.");
    }
  });
});
</script>
<!-- END GOOGLE CAPTCHA -->
```
---
layout: page
title: Contact
heading: Contact Me
subheading: Holla atcho girl.
weight: 4
---

<form action="https://getsimpleform.com/messages?form_api_token=83c40eb5dd82c054717f96436857d083" method="post">
  <!-- the redirect_to is optional, the form will redirect to the referrer on submission -->
  <input type='hidden' name='redirect_to' value='http://localhost:3000/contact-thanks.html' />
  <!-- all your input fields here.... -->
  <input type='text' name='Name' />
  <input type='text' name='Email' />
  <input type='textarea' name='Message' />
  <input type='submit' value='Submit Message' />
</form>

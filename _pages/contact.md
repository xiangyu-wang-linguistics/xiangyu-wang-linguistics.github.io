---
permalink: /contact/
title: "Contact"
description: "Contact Xiangyu Wang about linguistics research, collaboration, or academic questions."
author_profile: true
---

You are welcome to get in touch about research, collaboration, or academic questions. Fill in the form below, then select **Open email draft**. Your email app will open a message addressed to my UCSC account, where you can review and send it.

<form id="contact-form" class="contact-form" action="mailto:xwang469@ucsc.edu?subject=Website%20contact" method="post" enctype="text/plain" aria-describedby="contact-form-note">
  <label for="contact-name">Name</label>
  <input id="contact-name" name="name" type="text" autocomplete="name" maxlength="100" required>

  <label for="contact-email">Your email</label>
  <input id="contact-email" name="email" type="email" autocomplete="email" maxlength="254" required>

  <label for="contact-subject">Subject</label>
  <input id="contact-subject" name="subject" type="text" maxlength="120" required>

  <label for="contact-message">Message</label>
  <textarea id="contact-message" name="message" rows="8" maxlength="4000" required></textarea>

  <button class="btn btn--info" type="submit">
    <i class="fas fa-envelope" aria-hidden="true"></i>
    Open email draft
  </button>

  <small id="contact-form-note" class="contact-form__note">This form prepares a draft in your email app. It does not send the message automatically.</small>
</form>

If the form does not open your email app, write to [xwang469@ucsc.edu](mailto:xwang469@ucsc.edu) directly.

<script>
(function () {
  "use strict";

  var recipient = "xwang469@ucsc.edu";
  var form = document.getElementById("contact-form");

  if (!form) {
    return;
  }

  form.addEventListener("submit", function (event) {
    event.preventDefault();

    var formData = new FormData(form);
    var name = String(formData.get("name") || "").trim();
    var email = String(formData.get("email") || "").trim();
    var subject = String(formData.get("subject") || "").trim();
    var message = String(formData.get("message") || "").trim();
    var body = [
      "Name: " + name,
      "Reply email: " + email,
      "",
      message
    ].join("\n");
    var mailtoUrl = "mailto:" + recipient
      + "?subject=" + encodeURIComponent(subject)
      + "&body=" + encodeURIComponent(body);

    window.location.href = mailtoUrl;
  });
}());
</script>

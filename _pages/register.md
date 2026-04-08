---
title: Register
lang: en
alternate:
  hi: /hi/register/
---

<div class="container py-5">

{% assign lang = page.lang | default: site.lang | default: "en" %}
{% assign strings = site.data.strings[lang] %}

<div class="row">
  <div class="col-lg-10 mx-auto">
    <h1>{{ strings.register.heading }}</h1>

    <div class="alert alert-success mb-4">
      <strong>Registration Fee: ₹300.</strong> All participants receive a certificate of participation.
    </div>

    <p class="mb-3">
      <a href="{{ site.data.config.site.registration.form_url }}" class="btn btn-outline-primary" target="_blank" rel="noopener noreferrer">
        Open Registration Form
      </a>
    </p>

    <div class="alert alert-info mb-4">
      Pls fill this php form and put your name under student name, and event name as CRE COMPUTE, and event type as conference registration.
    </div>

    <div class="mb-4 text-center">
      <img src="{{ site.data.config.site.registration.payment_qr_url }}" alt="Kotak Mahindra Bank Mumbai payment QR code" style="max-width: 340px; width: 100%; height: auto;">
    </div>

    {% include components/embed-form.html url=site.data.config.site.registration.form_url %}
  </div>
</div>

</div>

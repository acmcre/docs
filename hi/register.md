---
title: पंजीकरण
lang: hi
permalink: /hi/register/
alternate:
  en: /register/
---

<div class="container py-5">

{% assign strings = site.data.strings.hi %}

<div class="row">
  <div class="col-lg-10 mx-auto">
    <h1>{{ strings.register.heading }}</h1>

    <div class="alert alert-success mb-4">
      <strong>पंजीकरण शुल्क: ₹300।</strong> सभी प्रतिभागियों को प्रमाणपत्र मिलेगा।
    </div>

    <p class="mb-3">
      <a href="{{ site.data.config.site.registration.form_url }}" class="btn btn-outline-primary" target="_blank" rel="noopener noreferrer">
        Registration Form खोलें
      </a>
    </p>

    {% include components/embed-form.html url=site.data.config.site.registration.form_url %}
  </div>
</div>

</div>

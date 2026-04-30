---
title: Event Flyer
lang: en
layout: flyer
permalink: /flyer/
---

<div class="flyer-logos">
  <img src="{{ site.data.config.organisers.host.logo | relative_url }}" alt="{{ site.data.config.organisers.host.name }}">
  <img src="{{ '/assets/images/organisers/acm-isigcse-768x256.jpg' | relative_url }}" alt="ACM iSIGCSE">
  <img src="{{ '/assets/images/organisers/acm-india-council.svg' | relative_url }}" alt="ACM India Council">
  <img src="{{ '/assets/images/organisers/acm-sigcse.png' | relative_url }}" alt="ACM SIGCSE">
</div>

<div class="flyer-header">
  <h1 class="flyer-title">{{ site.data.config.site.event_name }}</h1>
  <p class="flyer-subtitle">{{ site.data.config.site.tagline }}</p>
</div>

<div class="flyer-details">
  <div class="flyer-detail">
    <span class="flyer-detail-label">Date</span>
    <span class="flyer-detail-value">{{ site.data.config.site.date_display }}</span>
  </div>
  <div class="flyer-detail">
    <span class="flyer-detail-label">Time</span>
    <span class="flyer-detail-value">{{ site.data.config.site.time }}</span>
  </div>
  <div class="flyer-detail">
    <span class="flyer-detail-label">Venue</span>
    <span class="flyer-detail-value">{{ site.data.config.site.location.name }}</span>
  </div>
  <div class="flyer-detail">
    <span class="flyer-detail-label">Fee</span>
    {% if site.data.config.site.registration and site.data.config.site.registration.fee %}
      {% assign fee_text = site.data.config.site.registration.fee %}
    {% elsif site.data.config.site.registration and site.data.config.site.registration.free %}
      {% assign fee_text = "Free Registration" %}
    {% elsif site.data.config.site.registration and site.data.config.site.registration.form_url %}
      {% assign fee_text = "Registration Open" %}
    {% else %}
      {% assign fee_text = "See website for registration details" %}
    {% endif %}
    <span class="flyer-detail-value">{{ fee_text }}</span>
  </div>
</div>

<div class="flyer-highlights">
  <h2>What to Expect</h2>
  <ul>
    <li>Keynote talk</li>
    <li>Panel discussion on CS education</li>
    <li>Hands-on educator workshop</li>
    <li>Researcher workshop on paper writing</li>
    <li>Meet fellow educators and researchers</li>
  </ul>
</div>

<div class="flyer-cta">
  <div class="flyer-cta-left">
    <p class="flyer-cta-text">Register Now</p>
    <p class="flyer-url"><a href="https://forms.gle/wwrdQNRJYpffNKtb6" target="_blank" rel="noopener noreferrer">Register here</a></p>
{% if site.features.sponsors %}
    <div class="flyer-sponsor">
      <span>Sponsored by</span>
      <img src="{{ '/assets/images/sponsors/mphasis_f1_logo.png' | relative_url }}" alt="Mphasis">
    </div>
{% endif %}
  </div>
  <div class="flyer-qr">
    <img src="{{ '/assets/images/QR_burst.short.gy_acm-cre.svg' | relative_url }}" alt="QR Code to register">
  </div>
</div>

<div class="flyer-footer">
  Organised by {{ site.data.config.organisers.host.name }} & ACM India iSIGCSE
</div>

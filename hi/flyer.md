---
title: इवेंट फ्लायर
lang: hi
layout: flyer
permalink: /hi/flyer/
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
    <span class="flyer-detail-label">तिथि</span>
    <span class="flyer-detail-value">{{ site.data.config.site.date_display }}</span>
  </div>
  <div class="flyer-detail">
    <span class="flyer-detail-label">समय</span>
    <span class="flyer-detail-value">{{ site.data.config.site.time }}</span>
  </div>
  <div class="flyer-detail">
    <span class="flyer-detail-label">स्थान</span>
    <span class="flyer-detail-value">{{ site.data.config.site.location.name }}</span>
  </div>
  <div class="flyer-detail">
    <span class="flyer-detail-label">शुल्क</span>
    <span class="flyer-detail-value">{% if site.data.config.site.registration.free %}निःशुल्क पंजीकरण{% else %}पंजीकरण खुला है{% endif %}</span>
  </div>
</div>

<div class="flyer-highlights">
  <h2>क्या उम्मीद करें</h2>
  <ul>
    <li>मुख्य भाषण</li>
    <li>CS शिक्षा पर पैनल चर्चा</li>
    <li>शिक्षकों के लिए व्यावहारिक कार्यशाला</li>
    <li>शोधकर्ताओं के लिए पेपर लेखन कार्यशाला</li>
    <li>साथी शिक्षकों और शोधकर्ताओं से मिलें</li>
  </ul>
</div>

<div class="flyer-cta">
  <div class="flyer-cta-left">
    <p class="flyer-cta-text">अभी पंजीकरण करें</p>
    <p class="flyer-url">{{ '/hi/register/' | relative_url }}</p>
{% if site.features.sponsors %}
    <div class="flyer-sponsor">
      <span>प्रायोजक</span>
      <img src="{{ '/assets/images/sponsors/mphasis_f1_logo.png' | relative_url }}" alt="Mphasis">
    </div>
{% endif %}
  </div>
  <div class="flyer-qr">
    <img src="{{ '/assets/images/QR_burst.short.gy_acm-cre.svg' | relative_url }}" alt="पंजीकरण के लिए QR कोड">
  </div>
</div>

<div class="flyer-footer">
  आयोजक: {{ site.data.config.organisers.host.name }} और ACM India iSIGCSE
</div>

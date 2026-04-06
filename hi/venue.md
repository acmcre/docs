---
title: स्थान
layout: feature-page
feature: venue
lang: hi
permalink: /hi/venue/
alternate:
  en: /venue/
---

<div class="container py-5">

{% assign strings = site.data.strings.hi %}

<h1>{{ strings.venue.heading }}</h1>

<div class="row mb-5">
  <div class="col-lg-6 mb-4 mb-lg-0">
    <h2 class="h4">{{ site.data.config.site.location.name }}</h2>
    <p>
      {{ site.data.config.site.location.address }}
    </p>
    <p>
      <a href="{{ site.data.config.site.location.url }}" target="_blank" rel="noopener" class="btn btn-outline-primary btn-sm me-2">
        विश्वविद्यालय वेबसाइट पर जाएं
      </a>
      <a href="{{ site.data.config.site.location.map_url }}" target="_blank" rel="noopener" class="btn btn-outline-secondary btn-sm">
        Google Maps में खोलें
      </a>
    </p>
  </div>

  <div class="col-lg-6">
    {% if site.data.config.site.location.map_embed_url %}
      <div class="venue-map">
        <iframe
          src="{{ site.data.config.site.location.map_embed_url }}"
          title="स्थान का नक्शा"
          loading="lazy"
          allowfullscreen>
        </iframe>
      </div>
    {% endif %}
  </div>
</div>

<div class="alert alert-info mb-5">
  कार्यक्रम के दिन सहायता के लिए संपर्क करें: <a href="mailto:{{ site.data.config.site.social.email }}">{{ site.data.config.site.social.email }}</a>
</div>

<div class="row mb-5">
  <div class="col-lg-10">
    <h2 class="h4">{{ strings.venue.directions }}</h2>

    <div class="card border-0 bg-light mb-4">
      <div class="card-body">
        <h3 class="h5">विकल्प 1: एयरपोर्ट / रेलवे स्टेशन से</h3>
        <p>इंदौर शहर पहुंचने के बाद आप कैब, ऑटो या स्थानीय बस के माध्यम से कैंपस पहुंच सकते हैं।</p>

        <h4 class="h6 mt-3">देवी अहिल्याबाई होलकर एयरपोर्ट (इंदौर) से</h4>
        <ul>
          <li>एयरपोर्ट से ऐप कैब/टैक्सी लेकर सीधे {{ site.data.config.site.location.name }} पहुंचें।</li>
          <li>यात्रा समय ट्रैफिक के अनुसार बदल सकता है, इसलिए पर्याप्त समय लेकर निकलें।</li>
        </ul>

        <h4 class="h6 mt-3">इंदौर रेलवे स्टेशन से</h4>
        <ul>
          <li>स्टेशन से बाहर निकलकर कैब/ऑटो द्वारा कैंपस तक पहुंचें।</li>
          <li>बुकिंग के समय गंतव्य में {{ site.data.config.site.location.name }} दर्ज करें।</li>
        </ul>
      </div>
    </div>

    <div class="card border-0 bg-light mb-4">
      <div class="card-body">
        <h3 class="h5">विकल्प 2: कार या कैब से</h3>
        <p>Google Maps में {{ site.data.config.site.location.name }} खोजकर सीधे मार्ग प्राप्त करें।</p>
        <p class="mb-0"><strong>पार्किंग:</strong> कैंपस पर उपलब्धता के अनुसार पार्किंग व्यवस्था उपलब्ध रहेगी।</p>
      </div>
    </div>
  </div>
</div>

{% if site.data.config.site.accommodation.available %}
<div class="row mb-5">
  <div class="col-lg-8">
    <div class="card border-0 bg-light">
      <div class="card-body">
        <h2 class="h5 mb-3">आवास</h2>
        <p>यदि आपको आवास की आवश्यकता है, तो {{ site.data.config.site.accommodation.location }} में <strong>{{ site.data.config.site.accommodation.name }}</strong> उपलब्ध है।</p>
        <p class="mb-0"><strong>दर:</strong> {{ site.data.config.site.accommodation.price }}</p>
        <p class="small text-muted mt-3 mb-0">बुकिंग सहायता के लिए आयोजकों से संपर्क करें।</p>
      </div>
    </div>
  </div>
</div>
{% endif %}

</div>

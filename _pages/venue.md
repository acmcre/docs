---
title: Venue
layout: feature-page
feature: venue
lang: en
alternate:
  hi: /hi/venue/
---

<div class="container py-5">

{% assign lang = page.lang | default: site.lang | default: "en" %}
{% assign strings = site.data.strings[lang] %}

<h1>{{ strings.venue.heading }}</h1>

<div class="row mb-5">
  <div class="col-lg-6 mb-4 mb-lg-0">
    <h2 class="h4">{{ site.data.config.site.location.name }}</h2>
    <p>
      {{ site.data.config.site.location.address }}
    </p>
    <p>
      <a href="{{ site.data.config.site.location.url }}" target="_blank" rel="noopener" class="btn btn-outline-primary btn-sm me-2">
        Visit University Website
      </a>
      <a href="{{ site.data.config.site.location.map_url }}" target="_blank" rel="noopener" class="btn btn-outline-secondary btn-sm">
        Open in Google Maps
      </a>
    </p>
  </div>

  <div class="col-lg-6">
    {% if site.data.config.site.location.map_embed_url %}
      <div class="venue-map">
        <iframe
          src="{{ site.data.config.site.location.map_embed_url }}"
          title="Venue location map"
          loading="lazy"
          allowfullscreen>
        </iframe>
      </div>
    {% endif %}
  </div>
</div>

<div class="alert alert-info mb-5">
  For day-of assistance, contact <a href="mailto:{{ site.data.config.site.social.email }}">{{ site.data.config.site.social.email }}</a>
</div>

<div class="row mb-5">
  <div class="col-lg-10">
    <h2 class="h4">{{ strings.venue.directions }}</h2>

    <div class="card border-0 bg-light mb-4">
      <div class="card-body">
        <h3 class="h5">Getting Here</h3>
        <p>Add directions specific to your venue here. Consider including:</p>
        <ul>
          <li>Public transport options</li>
          <li>Driving directions and parking</li>
          <li>Shuttle services if available</li>
        </ul>
      </div>
    </div>
  </div>
</div>

{% if site.data.config.site.accommodation.available %}
<div class="row mb-5">
  <div class="col-lg-8">
    <div class="card border-0 bg-light">
      <div class="card-body">
        <h2 class="h5 mb-3">Accommodation</h2>
        <p>If you need accommodation, the <strong>{{ site.data.config.site.accommodation.name }}</strong> at {{ site.data.config.site.accommodation.location }} is available.</p>
        <p class="mb-0"><strong>Rate:</strong> {{ site.data.config.site.accommodation.price }}</p>
        <p class="small text-muted mt-3 mb-0">Contact the organisers for booking assistance.</p>
      </div>
    </div>
  </div>
</div>
{% endif %}

</div>

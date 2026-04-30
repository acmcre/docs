---
title: Spread the Word
lang: en
alternate:
  hi: /hi/spread-the-word/
---

<div class="container py-5">

{% assign lang = page.lang | default: site.lang | default: "en" %}
{% assign strings = site.data.strings[lang] %}

<h1>{{ strings.spread_the_word.heading }}</h1>

<p class="lead mb-4">Help us spread the word about {{ site.data.config.site.event_name }}!</p>

{% if site.features.flyer %}
<!-- Flyers Section -->
<div class="share-section">
  <h3>{{ strings.spread_the_word.flyer_section }}</h3>
  <p>Download our event flyers to share with your network:</p>
  <div class="flyer-cards">
    <div class="flyer-card">
      <a href="{{ '/flyer/?print=1' | relative_url }}" class="btn btn-outline-primary" target="_blank" rel="noopener">
        Generate English PDF
      </a>
      <a href="{{ '/flyer/' | relative_url }}" class="flyer-card-link">{{ strings.spread_the_word.view_browser }}</a>
    </div>
    <div class="flyer-card">
      <a href="{{ '/hi/flyer/?print=1' | relative_url }}" class="btn btn-outline-primary" target="_blank" rel="noopener">
        Generate हिंदी PDF
      </a>
      <a href="{{ '/hi/flyer/' | relative_url }}" class="flyer-card-link">{{ strings.spread_the_word.view_browser }}</a>
    </div>
  </div>
</div>
{% endif %}

<!-- Email Template Section -->
<div class="share-section">
  <h3>{{ strings.spread_the_word.email_section }}</h3>

  <h4 class="h6">{{ strings.spread_the_word.email_subject }}</h4>
  <div class="position-relative">
    <pre id="email-subject">Invitation: {{ site.data.config.site.event_name }} – Registration Open</pre>
    <button class="btn btn-sm btn-outline-secondary copy-btn position-absolute top-0 end-0 m-2"
            data-copy-target="email-subject"
            data-copied-text="{{ strings.spread_the_word.copied }}">
      {{ strings.spread_the_word.copy_button }}
    </button>
  </div>

  <h4 class="h6 mt-3">{{ strings.spread_the_word.email_body }}</h4>
  <div class="position-relative">
    <pre id="email-body">Dear colleagues,

I am writing to invite you to {{ site.data.config.site.event_name }}, a one-day gathering for CS educators and researchers hosted by {{ site.data.config.organisers.host.name }} and ACM India iSIGCSE.

Date: {{ site.data.config.site.date_display }}
Time: {{ site.data.config.site.time }}
Venue: {{ site.data.config.site.location.name }}

The day includes group-based sessions from Idea to Structure, mentoring breaks, and a final presentation of your idea and research plan.

Details and registration: https://forms.gle/wwrdQNRJYpffNKtb6

Best regards,
[Your name]</pre>
    <button class="btn btn-sm btn-outline-secondary copy-btn position-absolute top-0 end-0 m-2"
            data-copy-target="email-body"
            data-copied-text="{{ strings.spread_the_word.copied }}">
      {{ strings.spread_the_word.copy_button }}
    </button>
  </div>
</div>

<!-- Social Media Section -->
<div class="share-section">
  <h3>{{ strings.spread_the_word.social_section }}</h3>

  <h4 class="h6">{{ strings.spread_the_word.twitter_post }}</h4>
  <div class="position-relative">
    <pre id="twitter-post">{{ site.data.config.site.event_name }}

{{ site.data.config.site.date_display }}
{{ site.data.config.site.location.name }}

A day for CS educators and researchers: idea-to-structure workshop sessions, mentoring breaks, and peer connections.

Register here: https://forms.gle/wwrdQNRJYpffNKtb6

#CSEducation #ACMIndia</pre>
    <button class="btn btn-sm btn-outline-secondary copy-btn position-absolute top-0 end-0 m-2"
            data-copy-target="twitter-post"
            data-copied-text="{{ strings.spread_the_word.copied }}">
      {{ strings.spread_the_word.copy_button }}
    </button>
  </div>

  <h4 class="h6 mt-3">{{ strings.spread_the_word.linkedin_post }}</h4>
  <div class="position-relative">
    <pre id="linkedin-post">{{ site.data.config.site.event_name }} is a one-day regional gathering for CS educators and researchers.

Hosted by {{ site.data.config.organisers.host.name }} and ACM India iSIGCSE.

{{ site.data.config.site.date_display }}
{{ site.data.config.site.location.name }}

The programme includes:
– Session 1: Ideas that work
– Session 2: Ideas to Structure
– Session 3: Structure to Paper
– Session 4: Presentations and wrap-up
– Breaks with pre-scheduled 1-1 mentoring

Registration is open now: https://forms.gle/wwrdQNRJYpffNKtb6

#CSEducation #ACMIndia</pre>
    <button class="btn btn-sm btn-outline-secondary copy-btn position-absolute top-0 end-0 m-2"
            data-copy-target="linkedin-post"
            data-copied-text="{{ strings.spread_the_word.copied }}">
      {{ strings.spread_the_word.copy_button }}
    </button>
  </div>
</div>

</div>

<script>
document.querySelectorAll('.copy-btn').forEach(btn => {
  btn.addEventListener('click', function() {
    const targetId = this.getAttribute('data-copy-target');
    const text = document.getElementById(targetId).textContent;
    navigator.clipboard.writeText(text).then(() => {
      this.classList.add('copied');
      setTimeout(() => this.classList.remove('copied'), 2000);
    });
  });
});
</script>

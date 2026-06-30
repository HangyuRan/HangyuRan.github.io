<h2 id="publications" class="section-title publications-heading">Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li>
<div class="pub-row{% unless link.image %} pub-row-no-image{% endunless %}">
  {% if link.image %}
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% if link.conference_short %}
    <abbr class="badge">{{ link.conference_short }}</abbr>
    {% endif %}
  </div>
  {% endif %}
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      {% unless link.image %}
      {% if link.conference_short %}
      <span class="pub-badge-inline">{{ link.conference_short }}</span>
      {% endif %}
      {% endunless %}
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical">
        <span class="pub-venue">{{ link.conference }}</span>
        {% if link.notes %}
        <span class="pub-venue-note">{{ link.notes }}</span>
        {% endif %}
      </div>
    <div class="pub-links">
      {% if link.page %}
      <a href="{{ link.page }}" target="_blank">[Project]</a>
      {% endif %}
      {% if link.pdf %}
      <a href="{{ link.pdf }}" target="_blank">[Paper]</a>
      {% endif %}
      {% if link.code %}
      <a href="{{ link.code }}" target="_blank">[Code]</a>
      {% endif %}
      {% if link.demo %}
      <a href="{{ link.demo }}" target="_blank">[Demo]</a>
      {% endif %}
      {% if link.twitter %}
      <a href="{{ link.twitter }}" target="_blank">[Twitter]</a>
      {% endif %}
    </div>
    {% if link.others %}
    <div class="pub-meta-row">{{ link.others }}</div>
    {% endif %}
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>

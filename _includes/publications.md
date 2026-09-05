<h2 id="publications">Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}
<li>
  <div class="pub-row{% unless link.image %} no-image{% endunless %}">
    {% if link.image %}
    <div class="pub-teaser-wrap">
      <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" alt="{{ link.title }}">
      {% if link.conference_short %}<abbr class="badge">{{ link.conference_short }}</abbr>{% endif %}
    </div>
    {% endif %}

    <div class="pub-content">
      <div class="title">
        {% if link.page %}<a href="{{ link.page }}" target="_blank" rel="noopener">{{ link.title }}</a>
        {% elsif link.pdf %}<a href="{{ link.pdf }}" target="_blank" rel="noopener">{{ link.title }}</a>
        {% else %}{{ link.title }}{% endif %}
      </div>
      {% if link.authors %}<div class="author">{{ link.authors }}</div>{% endif %}
      {% if link.conference %}<div class="periodical"><em>{{ link.conference }}</em></div>{% endif %}
      <div class="links">
        {% if link.pdf %}<a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" target="_blank" rel="noopener">PDF</a>{% endif %}
        {% if link.arxiv %}<a href="{{ link.arxiv }}" class="btn btn-sm z-depth-0" target="_blank" rel="noopener">arXiv</a>{% endif %}
        {% if link.code %}<a href="{{ link.code }}" class="btn btn-sm z-depth-0" target="_blank" rel="noopener">Code</a>{% endif %}
        {% if link.page %}<a href="{{ link.page }}" class="btn btn-sm z-depth-0" target="_blank" rel="noopener">Page</a>{% endif %}
        {% if link.notes %}<strong><i class="pub-note">{{ link.notes }}</i></strong>{% endif %}
      </div>
      {% if link.others %}<div class="pub-others">{{ link.others }}</div>{% endif %}
    </div>
  </div>
</li>
{% endfor %}

</ol>
</div>

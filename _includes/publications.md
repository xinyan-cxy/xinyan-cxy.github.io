<h2 id="publications" style="margin: 2px 0px -15px;">Publications and Preprints</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if link.image %} 
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width: 100%;">
    {% endif %}
    {% if link.conference_short %} 
    <abbr class="badge">{{ link.conference_short }}</abbr>
    {% endif %}
  </div>

  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical">
        <em>
        {% if link.conference %}
          {{ link.conference }}
        {% elsif link.conference_short %}
          {{ link.conference_short }}
        {% endif %}
        </em>
      </div>

    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      
      {% if link.project %} 
      <a href="{{ link.project }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      
      {% if link.dataset %} 
      <a href="{{ link.dataset }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Dataset</a>
      {% endif %}

      {% if link.benchmark %} 
      <a href="{{ link.benchmark }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Benchmark</a>
      {% endif %}
      
      {% if link.notes %} 
      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      
    </div>
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>

# Jekyll-website
List
- [Blog](https://jaspervincent.github.io)
- [test](https://{{ site.url }}/archive.html)


<nav>
  site.url: {{ site.url }}
  site.baseurl: {{ site.baseurl }}<br>
  page.url: {{ page.url }} <br>
  
  {% assign baseurl = "/jekyll-website" | join: page.url %}
  baseurl: {{ baseurl }}
  
  {% for item in site.nav %}
    <a href="{{ item.link }}" 
      {% if  baseurl == item.link %} style="color: red;" {% endif %}
    >
      {{ item.name }} -- 
    </a>
  {% endfor %}
</nav>

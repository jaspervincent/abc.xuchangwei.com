# Jekyll-website
List
- [Blog](https://jaspervincent.github.io)
- [jekyll-website](https://jaspervincent.github.io/jekyll-website)
- [hugo-website](https://jaspervincent.github.io/hugo-website)

- [jekyll-归档]({{ site.url }}{{ site.baseurl }}/archive.html)
- [hugo-归档](https://jaspervincent.github.io/hugo-website/tags/)

<nav>
  site.url: {{ site.url }}<br>
  site.baseurl: {{ site.baseurl }}<br>
  page.url: {{ page.url }} <br>
  
  {% assign baseurl = "/jekyll-website" | join: page.url %}
  baseurl: {{ baseurl }}<br>
  
  {% for item in site.nav %}
    <a href="{{ item.link }}" 
      {% if  baseurl == item.link %} style="color: red;" {% endif %}
    >
      {{ item.name }} -- 
    </a>
  {% endfor %}
</nav>

# Jekyll-website
List
- [Blog](https://jaspervincent.github.io)
- [归档]({{ site.url }}{{ site.baseurl }}/archive.html)


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

# Jekyll-website
List
- [Blog](https://jaspervincent.github.io)
<nav>
  {% for item in site.nav %}
    <a href="{{ item.link }}" 
      {% if page.url == item.link %} style="color: red;" {% endif %}
    >
      {{ item.name }}
    </a>
  {% endfor %}
</nav>

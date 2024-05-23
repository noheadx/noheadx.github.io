{% for category in site.categories reversed %}
  <h4>{{ category[0] }}</h4>
<ul>
  {% for post in category[1] %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}, {{ post.date | date_to_string }}</a>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>
{% endfor %}
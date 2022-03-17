---
layout: default 
title: "Whoami"
---

![avatar]({{ site.url }}/assets/img/avatar.png){: style="width:50px;display: block;margin-left: auto;margin-right: auto;"}  
_I know it's hard - being a leader is..._ that's one of my most memorable movie quotes because that's how people used to look at leadership: it's exhausting, painful, comes with a price, you're lonely up there yaddiyaddi...

No! It doesn't need to be hard, exhausting or painful and your definitely not a good leader if you're all alone. It's just one of the things that are necessary to make companies successful. I write about all the things that I think are necessary to make a company successful in this blog - just sharing my views.

{% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
<ul>
  {% for post in category[1] %}
    <li>
      <a href="{{ post.url }}">{{ post.date | date_to_long_string }} - {{ post.title }}</a>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>
{% endfor %}
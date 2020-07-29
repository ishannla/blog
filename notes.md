---
---

{% for post in site.posts %}

  {% if post.path contains 'notes' %}

  <li class="posts-list-item">
    <div class="posts-list-title">
      <h3 class="title">
        <a href="{{ post.url }}">
          {{ post.title }}
        </a>
      </h3>
      <span style="margin-left:0px" class="timestamp timestamp-inline">
        {% include post-date.html %}
      </span>
    </div>
  </li>

  {{ post.content | strip_html | truncatewords: site.notes_word_count }} [Read more]({{ post.url }})

  {% endif %}

{% endfor %}
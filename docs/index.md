
<ul>
{% for version_hash in site.data.versions %}
{% assign version = version_hash[1] %}
{% for entries_hash in version %}
{% assign entry = entries_hash[1] %}
  <li>
    <a href="https://github.com/{{ org.username }}">
      {{ entry[0].name }}
      {{ entry[0].version }}
    </a>
    ({{ entry | size }} entry)
  </li>
{% endfor %}
{% endfor %}
</ul>
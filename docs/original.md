
<ul>
{% for version_hash in site.data.versions %}
{% assign version = version_hash[1] %}
  <li>
    <a href="https://github.com/{{ org.username }}">
      {{ version.name }}
    </a>
    ({{ .index | size }} entries)
  </li>
{% endfor %}
</ul>

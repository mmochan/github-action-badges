
<ul>
{% for version_hash in site.data.versions %}
{% assign version = version_hash[1] %}

{% for entries_hash in version %}
{% assign entry = entries_hash[1] %}

{% for helm_hash in entry %}
{% assign helm = helm_hash[1] %}

{% for helm_version_hash in helm %}
{% assign helm_version = helm_version_hash[1] %}
  <li>
    <a href="https://github.com/{{ org.username }}">
      {{ helm_version }}
      <!-- {{ helm_version.version }} -->
    </a>
    <!-- ({{ helm_version | size }} helm_version) -->
  </li>
{% endfor %}
{% endfor %}
{% endfor %}
{% endfor %}
</ul>
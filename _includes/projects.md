
{% for group in projects %}
## {{ group.group_name }}
{% for repo in group.repos %}
* {% if repo.repo_name %} {{ repo.repo_name }} <object data="assets/shields/{{ repo.repo_name | split: '/' | join: '-' }}.svg" type="image/svg+xml" align="top"></object> {% endif %} {% if repo.repo2_name %} {{ repo.repo2_name }} <object data="assets/shields/{{ repo.repo2_name | split: '/' | join: '-' }}.svg" type="image/svg+xml" align="top"></object> {% endif %} {% if repo.web_name %}<a href="{{ repo.web_url }}" target="blank">{{ repo.web_name }}</a>{% endif %} {% if repo.web2_name %}<a href="{{ repo.web2_url }}" target="blank">{{ repo.web2_name }}</a>{% endif %} {{ repo.content }} {% endfor %}
{% endfor %}



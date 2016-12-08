---
---
#### cours collection

Dans le _config.yml :

  * collections:
      cours:
       output: true

Dans l'endroit ou l'on veut que cela apparaisse :

  * {% for cour in site.cours %}
      <li>
       <img src="{{ cour.thumbnail-path }}" alt="{{ cour.title }}"/>
       <a href="{{ cour.url }}">{{ cour.title }}</a>
      </li>
    {% endfor %}


---
---
#### Cours Jekyll

       * jekyll serve (arreter -> ctrl c)
       * boucle de navigation dans un <na>
       * ajouter un titre a toutes les pages a ajouter
       * ajouter "navigation_weight(numero de la page)"
       * toutes modif dans le fichier _config.yml demande de relancer le serveur
          *    <ul>
                   {% assign navigation_pages = site.html_pages |                    sort: 'navigation_weight' %}
                   {% for p in navigation_pages %}
                   {% if p.navigation_weight %}
                  <li>
                    <a href="{{ p.url }}" {% if p.url == page.url %}class="active"{% endif %}>
                    {{ p.title }}</a>
                 </li>
                   {% endif %}
                   {% endfor %}
               </ul>
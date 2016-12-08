# flatfiles
#### Cours sur le GitHub

->flatfiles
    *  _includes      =diviser la page en plusieurs parties et les inclure dans la page 
    *  _layout        = squelette de la page sans contenu
    *  cours
    *  tumblr
    *  _config.yml    =base de donnée
    *  index.html     =contenue de la page
    *  README.md
    *  _nomdufichier  =tout ce qui a « _ » n’est pas généré par Jekyll

#### Commandes Git

* Récuperer un file dans GitHub → git clone…. (URL)
* Synchroniser des fichiers :
       * git init (flafiles)
       * git add … (nom du fichier à ajouter)
       * git commit - « message » (changement apporté)
       * git status (vérification des données)
       * git push (-u origin master)    synchroniser/envoie !
       
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

---
layout: page
title: Equipe
navigation_weight: 3
---

{% for member in site.data.members %}
   nom : {{ member.nom }} 
   hobbies : {{ member.hobbies }} 
   cursus : {{ member.cursus }}
   motivation : {{ member.motivation }}
   avatar : 
   ![avatar]({{member.avatar}})
{% endfor %}


{% for club in site.data.club %}
{% for clubo in club[1]%}
   {{clubo.key}}
{% endfor %}
{% endfor %}


---
---
####Cours data
  données à rentrer :
  - nom: Benjamin Gasnier (une entrée)
  hobbies: modélisme
  cursus: lol
  motivation: dominer le moooooooonde
  avatar
  
  -boucle :
  {% for member in site.data.members %}
   nom : {{ member.nom }} 
   hobbies : {{ member.hobbies }} 
   cursus : {{ member.cursus }}
   motivation : {{ member.motivation }}
   avatar : 
   ![avatar]({{member.avatar}})
{% endfor %}
  
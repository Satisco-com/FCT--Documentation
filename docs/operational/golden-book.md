---
layout: default
title: Golden Book
nav_order: 1300
permalink: /docs/operational/golden-book
---

# Golden Book - Nos histoires en or

## ADA - Un processus pour plusieurs actions


{: style="text-align: justify" }
En 2017, j'ai eu la chance de pouvoir travailler sur l'optimisation d'un Framework dont les performances ne correspondaient pas à ce qui était attendu du client.
J'ai commencé par modifier l'orchestration des logiciels entre eux et après avoir obtenu des résultats satisfaisant, je me suis penché sur l'architecture logique.

{: style="text-align: justify" }
A l'origine, il n'était possible d'executer qu'une seule action par processus. Mon idée était donc de permettre un nombre ilimité d'actions pour un seul et même processus.
Ceci permettait de donner la mains à l'utilisateur, qui pourrait choisir de rester comme avant ou alors d'utiliser cette nouvelle fonctionalité.

{: style="text-align: justify" }
Je devais cependant vérifier l'équilibre entre **fonctionalité** et **maintenance** car je ne voulais pas ajouter des fonctionalités au détriment de la complexité tant pour l'utilisateur que pour le developpeur.
Le développement, bien qu'un peut complexe, s'est bien passé et les premiers résultats sont tombés très vite. Les performances étaient augmentées de 50% par rapport à mes propres chiffres obtenu précédemment.

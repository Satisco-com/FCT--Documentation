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
J'ai commencé par modifier l'orchestration des logiciels entre eux et après avoir obtenu des résultats satisfaisants, je me suis penché sur l'architecture logique.

{: style="text-align: justify" }
A l'origine, il n'était possible d'executer qu'une seule action par processus. Mon idée était donc de permettre un nombre ilimité d'actions pour un seul et même processus.
Ceci permettait de donner la main à l'utilisateur, qui pourrait choisir de rester comme avant ou alors d'utiliser cette nouvelle fonctionalité.

{: style="text-align: justify" }
Je devais cependant vérifier l'équilibre entre **fonctionalité** et **maintenance** car je ne voulais pas ajouter des fonctionalités au détriment de la complexité tant pour l'utilisateur que pour le developpeur.
Le développement, bien qu'un peu complexe, s'est bien passé et les premiers résultats sont tombés très vite. Les performances étaient augmentées de 50% par rapport à mes propres chiffres obtenu précédemment.



## ADA/JTSO - La gestion des données de sortie

{: style="text-align: justify" }
Depuis 2015 et jusqu'en 2023, la gestion des données de sortie d'une map ITX se faisait via un mode inline qui s'appel "echo sized data".
Il permettait de récupérer en mémoire sous un format "4 TOTO" (numberOfByte space bytes) la sortie d'une map executée.
Le risque majeur de cette méthode est la confusion des données de sortie multiple. Il est impossible de certifier que la donnée A appartient bien à la carte de sortie numéro 5.

{: style="text-align: justify" }
Le second risque de cette méthode est la consommation mémoire non maitrisée par le Framework.
Une map ITX est statique, c'est à dire qu'une fois démarrée, il ne sera plus possible de modifier son execution.
Si celle-ci doit retourner 1Go de données, le Framework sera dans l'obligation de charger 1Go de données en mémoire.

{: style="text-align: justify" }
De nombreux tests effectués ont permet de démontrer les avantages d'un mode "file system" sur un gros volume de messages, tant en performances qu'en consommation mémoire.
C'est donc en 2023 que cette nouvelle logique sera implémentée.

{: style="text-align: justify" }
Il est cependant important de comprendre qu'un équilibre existe entre ces deux modes de fonctionnement et le volume de messages. Le mode "file system" n'est pas **LA** solution à tous mais le mode "echo sized data" non plus.
Cependant les risques présents sur le mode "echo sized data" restent importants, il faut étudier un mode hybride où la donnée de sortie contiendrait un header permettant d'identifier le nom de la donnée.

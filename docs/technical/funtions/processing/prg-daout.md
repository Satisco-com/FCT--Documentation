---
layout: default
title: DAOUT
nav_order: 300
parent: Processing
grand_parent: Functionalities
permalink: /docs/functionalities/processing/daout
---


# Data Output

## Presentation

<p align="center"><img src="../../../assets/img/functions/Functions-Processing-2.png" width="400"></p>

{: style="text-align: justify" }
**Gérer des données de sortie d'une Action** est une des fonctionnalité fondamentale de **SAI**.
Elle permet de gérer la transformation ou le routage de données via le setup.

## Détails Techniques

{: style="text-align: justify" }
Dans un premier temps, les sorties seront traitées de manière automatiques dans un mode "fichier". L'idée est que l'utilisateur définiera sa donné de sortie en deux temps. D'abord via une *technical reference* sur la carte de sortie concernée qui servira de liens vers ensuite une *Data* liée cette fois à l'*Action* dans laquelle il sera possible de fournir plus de détails la concernant.
>*Cette particularité est le résultat d'une expérience professionnelle précédente que vous pouvez retrouver [dans le Golden Book](../../../../FCT--Documentation/docs/operational/golden-book/#ADA/JTSO - La gestion des données de sortie)*

{: style="text-align: justify" }
Il est ici question d'une fonctionalité inédite. L'idée chaque sortie d'une action a un nom unique grâce au DataModel.
>**Note**: ce nom unique l'est dans tout le modèle et pas seulement pour le contexte de l'action, le stage ou le scenario.


## Pros & Cons

{: style="text-align: justify" }
L'identification unique d'une donnée permet de la partager entre deux *Actions* et ce même si ces actions ne se suivent pas dans un même processus.
Le Processing n'a donc plus à traiter les données mais uniquement son identifiant, il consomme donc beaucoup moins de mémoire.


## SAI Identifier

{: style="text-align: justify" }
Cette fonctionalité sera identifier plus tard sous le nom de **DAOUT**. Tout ce qui concerne donc les test parts, les codes error ou warning et tous liens avec celle-ci seront docn mentionnés avec **DAOUT**.

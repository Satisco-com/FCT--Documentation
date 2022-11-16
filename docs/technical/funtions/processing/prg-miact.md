---
layout: default
title: MIACT
nav_order: 100
parent: Processing
grand_parent: Functionalities
permalink: /docs/functionalities/processing/MIACT
---


# Multiple Actions

## Presentation

<p align="center"><img src="../../../assets/img/functions/Functions-Processing-1.png" width="400"></p>

{: style="text-align: justify" }
**Executer une ou plusieurs actions**, c'est **LA** fonctionalité primaire de SAI.
Son but est de pouvoir executer une ou plusieurs actions à la suite, c'est à dire dans une seule et même execution de Processing.


## Pros & Cons

{: style="text-align: justify" }
L'avantage d'une telle fonctionalité est tout d'abord l'impact sur les performances. En effet, plus besoin de sortir du process d'execution, écrire puis lire des données qui ont déjà été lues.
Cette fonctionnalité est le résultat d'une expérience professionnelle précédente que vous pouvez lire [dans le Golden Book Link](/FCT--Documentation/docs/operational/golden-book/#ADA - Un processus pour plusieurs actions)

{: style="text-align: justify" }
La fonctionalité peut sembler simple et c'est le cas, cependant elle induit une complexité suplémentaire sur d'autres fonctionalités:
1. La gestion d'error et d'événement afin de continuer ou non le flux
2. Le monitoring à gérer en temps réel ou à la fin de chaque processus


## SAI Identifier

{: style="text-align: justify" }
Cette fonctionalité sera identifier plus tard sous le nom de "MIACT". Tout ce qui concerne donc les test parts, les codes error ou warning et tous liens avec celle-ci seront docn mentionnés avec MIACT.

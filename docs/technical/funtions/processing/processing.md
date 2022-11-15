---
layout: default
title: Processing
nav_order: 100
parent: Functionalities
has_children: true
permalink: /docs/functionalities/processing
---

# Processing

## Presentation

**SAI** ne contient pas beaucoup de composants framework et le _Processing_ est l'un d'eux.
Ce _Processing_ a une particularité car même en admettant que **SAIF** soit principalement conçu avec **ITX**, il est possible d'avoir plusieurs Processing dans **SAI**.
>**Exemple:** Un processing ITX principal, un Processing SBI secondaire et un Processing Java tiers.

Le _Processing_ a pour but principal d'executer les maps business dans un contexte et une configuration défini via le Core Model.
C'est donc à lui qu'incombe le travail de récupérer les données de sorties, s'il y en a, et de les transmettre au composant suivant.

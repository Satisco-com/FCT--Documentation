---
layout: default
title: Grey - Tools
parent: Core Model
grand_parent: Data Model
nav_order: 9
---

# Tools #

## Introduction
<p align="center"><img src="../../../../assets/img/data-model/Tools.png" width="600"></p>


## Transform Format et Code
Le but de ces tables est de mettre à disposition de possibles table de transco ou de paramètres pour les flux business.
Un format sera défini par exemple en JSON et affichera via l'IHM l'équivalent d'une vue database. Le développeur pensera coder une table alors qu'en fait ça sera la table de code.
La table de code pourrait contenir beaucoup de colonnes anonymisées "colonne_1...". Il faut bien prévoir les colonnes indexées au risque de perdre des performances de recherche.

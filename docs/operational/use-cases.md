---
layout: default
title: Use Cases
nav_order: 1200
permalink: /docs/operational/use-cases
---

# Que sait faire SAI?

## Cas N°1: Excel mon beau excel!

Vous recevez de multiples clients, des factures toutes dans un format différent:
- Les dates sont reçues au format "31/12/2022" ou "31-12-22".
- Les sommes ont un séparateur de miliers, les décimales sont séparées parfois par une virgule, parfois par un point.
- Les sommes, la référence de l'article ou encore sa quantité ne sont pas dans la même colonne.
Afin de déclarer ces factures en interne, elles doivent être normées dans un fichier excel pour être importées dans un logiciel de facturation.
Ce cas est extremement consommateur de temps et générateur d'erreurs car un prix pourrait être confondu avec une référence par exemple.
En cas d'erreur, sa détection est parfois tardive et son impact grossit en fonction de ce délai.

SAI dans ce cas permet de:
- Définir votre traitement en fonction du client.
- Transformer le fichier reçu dans le fichier excel au format souhaité.
- Définir des calculs complexes et aller rechercher des informations provenant d'un autre système (SAP).
- Envoyer ce fichier à plusieurs destinataires (une équipe par email ou un logiciel tiers comme SAP directement).
- Alerter en cas d'erreur d'autres destinataires (le client source, une personne en particulier).
- Relancer le traitement une heure plus tard à cause d'un facteur externe.
- Traiter les fichiers à une heure ou date données.
- Conserver les fichiers en cas d'arrêt du système en attendant de les traiter.


## Cas n°2: Budget, je te couperai

Les employés utilisent un logiciel de pointage qui permet ensuite de calculer les budgets en fonction des projets pointés.
Ces employés travaillent parfois sur plusieurs projets en même temps et le pointage qui en découle est complexe.
Les projets sont défini par ordre de priorité et forcent le découpage des heures par exemple:
- Sur une journée de 8h.
- Le projet B est prioritaire.
- L'employé pointe de 8h à 12h sur le projet A et de 14h à 18h sur le projet C.
- Cependant pendant cette journée, il passe aussi 2 fois 1h sur le projet B.
On se retrouve donc avec un chevauchement des heures projets, une découpe est nécessaire afin d'obtenir:
- Projet A de 10h à 12h.
- Projet C de 14h à 18h.
- Projet B de 8h à 10h.
Ce genre d'opération se complexifie en fonction du nombre d'employés et de projets et peut vite être source d'erreurs.

SAI dans ce cas permet de:
- S'assurer que le calcul est bien fait.
- Changer dynamiquement les priorités projets et impacter automatiquement les calculs.
- Gagner du temps (si les projets sont des absences ou des maladies, cela devient bénéfique pour la génération de la paye).


## Cas n°3: Le coupe-file

Parfois un traitement est prioritaire car c'est une erreur grave ou un client VIP.
Si la demande est reçue par email, elle peut passer inaperçue un certain temps.

SAI dans ce cas permet de:
- Définir une priorité en fonction de conditions comme l'émetteur ou des données dans le fichier.


## Cas n°4: Je connais la chanson

Le BlackFriday approche et je dois préparer, comme chaque année, la mise à jours des prix et les promotions qui seront appliquées pendant cette période.
Je sais que chaque année, j'ai des erreurs de prix qui sont commises, plus ou moins graves car l'action finale est manuelle.
Le problème est que lorsque ces erreurs de prix arrivent, les commandes sont envoyées si rapidement qu'entre l'alerte et la correction, certaines ont déjà été envoyées et ne sont donc plus annulables. C'est une perte de bénéfices.

SAI dans ce cas permet de:
- Automatiser l'action finale et les vérifications qui en découlent.
- Automatiser l'analyse de commande et la validation du prix final avant son envoi.
- Alerter en temps réel sans impacter les temps de commande.

---
layout: default
title: Green - Processing
parent: Core Model
grand_parent: 5-Data Model
nav_order: 1
---

# Processing #

## Introduction ##
<p align="center"><img src="../../assets/img/data-model/Processing.png" width="500"></p>

Le __Processing__ c'est le coeur de __FCT__. Il est né d'abord de ce qui était le __Brouteur__ dans __FCT__. Il a ensuite évolué avec les années afin d'arriver petit à petit à un __système complet__ de Processing.
Il y a une tendance à confondre le __Processing__ avec __FCT__, c'est normal car il contenait aussi à l'origine une fonctionnalité de __Matching__ qui a cependant été supprimé dans les évolutions pour implémenter un composant à part entière.

Le principe de base du __Processing__ est de pouvoir executer une ou plusieurs activités à la suite. D'un point de vue __ITX__, cela sera représenté par __l'execution d'une ou plusieurs maps__ où il sera possible d'échanger des données entre chacun d'entre elle.
> **Example:** La réception d'un fichier EDIFACT transformé tout d'abord dans un format Pivot XML puis intégré dans un backend client


Le __second__ principe __important__ est de garder la possibilité de __réutilisabilité__ des activités et des scénario.
> **Example:** Une activité d'encodage en Latin-1 disponible pour tous
> **Example:** Un scénario d'intégration de fichier EDIFACT de type IFTMBF commun à tous client

## Scenario ##
Cette table était dans une version beta de FCT, une table de jonction entre un Assembly et un Stage et permettait la __réutilisabilité__ d'un groupe de Stage et donc d'Action.
__L'évolution__ de FCT a permis __d'affranchir__ l'interraction entre un __Assembly__ et les informations __fonctionnelles Partner et Message__.

Un __Scenario__ représente donc aujourd'hui __un ou plusieurs Stage__ qui peuvent avoir des types différents.
Son but est de permettre la __réutilisatibité__ d'un __process__ en entier pour un __Partner et un Message différent__.

## Stage ##
De différent types possible, il __représente une ou plusieurs Action__ dans un ordre défini.

Un type __Primary__ sera __obligatoire__ puisque ce sera le __premier__ à être exécuté. Il sera impossible sans lui de remonter ou traiter un événement ou une transformation.
Un type __Standard__ permettera d'effectuer des __traitements supplémentaires__ comme un traitement __post communication__.
> **Example:** Le message sortant a été envoyé au client, je lance une action de mise à jour du backend

Il pourra aussi permettre des traitements __parallèles__.
> **Example:** Je reçois un fichier contenant des centaines de factures qui doivent être envoyées séparément au client.

Un type __Event__ aura pour but une gestion __événementielle__ durant le process.
> **Example:** Des erreurs sont détectées sur plusieurs lignes du fichier entrant. Elles sont isolées puis renvoyées à la source pour information mais le process continue son traitement.

## Staction ##
C'est une __table de jonction__ permettant ainsi la __réutilisabilité d'Actions__ dans un __contexte__ ou un __ordre différent__.

## Action ##
C'est ici encore une __table de jonction__ mais avec un but un peu plus profond. Il n'est pas seulement question de __réutilisabilité__ mais aussi de __permission__.
Elle permet non seulement d'utiliser une même __map ITX__ dans des configurations différentes mais aussi d'ouvrir __FCT à d'autres logiciels__ sans avoir à modifier le fondement du framework.
> **Example:** Un client Satisco utilise un modèle équivalent avec ITX mais aussi avec SBI. Une action est donc aussi une action SBI.

## Data ##
Elle est apparue lors de la révision du modèle __, version 2.0.0__ lors de l'étude de la __problématique__ concernant la partie __Routing__.
L'idée était de rassembler les fonctionalités de Matching et Routing mais pour cela nécessitait de supprimer les liens vers Processing, ITX et Communication.
Cette table sera une des __rare contrainte__ pour les __dévelopeurs__ car elle nécessitera certainement un format spécifique pour le framework afin de parser correctement les données et paramètres.
Son but est de permettre __l'identification__ précise d'une __données de sortie__ et ainsi ne plus la lier forcément à une carte de sortie physique ITX.
Nous pourrons ensuite définir un __identifiant de groupe__ soit pour de l'envoie groupé. L'identifiant sera une clé primaire et permettra la garantie d'unicité.
> **Example:** Le serveur d'un client n'accepte que 10 connexions en parallèles. L'envoie est donc groupé pour diminuer le nombre de connexions simultanées.

ou encore pour prévoir l'envoie de fichiers provenant de scénario différent
> **Example:** Un client qui ne souhaite recevoir toute ses factures en même temps
> **Example:** Un marketplace qui souhaite recevoir la commande d'un client 1 et 2 en même temps

__L'événementiel__ sera lui aussi traité via la table Data. Il sera ainsi possible de traiter une __sortie__ en plus d'un __événement__.

---
layout: default
title: Lesson Learned
nav_order: 7200
has_children: true
parent: 10-Testing
permalink: /docs/testing/lesson-learned
---

# Lesson Learned

## Presentation

Le développement d'un Framework comme tout autre logiciel ou code informatique ne se fait jamais sans erreur.
Il est important, pour ne pas dire obligatoire, que chacune des erreurs rencontrées pendant le développement de SAIF soient répétoriées et définie comme une leçon apprise.

Chaque leçon donnera donc lieu à la création d'un code spécifique ainsi qu'un test dédié.
Ainsi, lors des tests de regression, nous garantirons la stabilité du framework par non seulement les tests de fonctionalité mais aussi par les tests d'erreur et/ou de bogues.


## Normalisation

Afin de bien documenter les leçons apprises et ainsi faciliter les échanges à ce sujet, une convention de nommage sera défini comme suit:
- "[A-Z]{3}" 3 lettres majuscules pour le type de code (CER pour CodeError, CWG pour CodeWarning)
- "-" en séparateur
- "[A-Z]{3}" 3 lettres majuscules pour le nom du composant SAIF
- "-" en séparateur
- "[A-Z]{5}" 5 lettres majuscule pour la fonctionalité SAIF
- "-" en séparateur
- "[0-9]{5}" 5 chiffres pour le numéro du test

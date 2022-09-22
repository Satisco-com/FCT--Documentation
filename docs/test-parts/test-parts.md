---
layout: default
title: Test Parts
nav_order: 6
permalink: /docs/test-parts
---

# Test Parts

## Presentation

Ici nous allons documenter l'intégralité des tests qui seront créés pour SAI.
Chaque fonctionalité SAI pourra résulter un ou plusieurs tests afin de garantir que SAI répond au besoin décrit.

Le regroupement de ces tests permettera aussi de valider toute possiblité de regression lors d'un nouveau developpement.
Chaque test devra être executer dans un contexte stable et constant, ainsi que son résultat.
La comparaison se fera sur le maximum de valeur possible mais certaines comme la date du jour où certains ID ne le pourront pas.


## Normalisation

Afin de bien documenter les tests et ainsi faciliter les échanges à ce sujet, une convention de nommage sera défini comme suit:
- "TPT" pour indiquer un test part
- "-" en séparateur
- "[A-Z]{3}" 3 lettres majuscules pour le nom du composant SAIF
- "-" en séparateur
- "[A-Z]{5}" 5 lettres majuscule pour la fonctionalité SAIF
- "-" en séparateur
- "[0-9]{5}" 5 chiffres pour le numéro du test

## Liste

| Test ID   	| Description  	| Lesson Learned  	| Initial Date  	|
|---	|---	|---	|
| TPT-PRG-MIACT-00001  	| Execute one action  	|    | 16 Sept 2022  	|
| TPT-PRG-MIACT-00002  	| Map not found  	| CER-ITX-IEXEC-00003   | 16 Sept 2022  	|
| TPT-PRG-MIACT-00003  	| Map failed  	| CER-ITX-IEXEC-00076   | 16 Sept 2022  	|
| TPT-PRG-MIACT-00004  	| Invalid command  	| CER-ITX-IEXEC-00065   | 16 Sept 2022  	|
| TPT-PRG-MIACT-00005  	| Action not found  	| CER-PRG-MIACT-00001   | 16 Sept 2022  	|
| TPT-PRG-MIACT-00006  	| Map warning  	| CWG-ITX-IEXEC-00021   | 17 Sept 2022  	|
| TPT-PRG-MIACT-00007  	| Stage not found  	| CER-PRG-MIACT-00002   | 17 Sept 2022  	|
| TPT-PRG-MIACT-00008  	| Execute two actions  	|    | 17 Sept 2022  	|
| TPT-PRG-MIACT-00009  	| Execute ten actions  	|    | 20 Sept 2022  	|
| TPT-PRG-MIACT-00010  	| Execute from action 3  	|    | 20 Sept 2022  	|



| Test ID   	| Description  	| Lesson Learned  	| Initial Date  	|
|---	|---	|---	|
| TPT-PRG-TEREF-00001  	| Fail on Warn Control Option  	|    | 21 Sept 2022  	|
| TPT-PRG-TEREF-00002  	| Trace Control Option  	|    | 21 Sept 2022  	|
| TPT-PRG-TEREF-00003  	| AuditLog Control Option  	|    | 22 Sept 2022  	|
| TPT-PRG-TEREF-00004  	| Data Audit Settings Control Option  	|    | 22 Sept 2022  	|

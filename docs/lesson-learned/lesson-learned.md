---
layout: default
title: Lesson Learned
nav_order: 7
permalink: /docs/lesson-learned
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

## Liste
Official IBM Documentation for ITX Codes: https://www.ibm.com/docs/en/ste/10.1.1?topic=messages-map-execution-error-warning

| Lesson ID   	| Description  	| Initial Date  	|
|---	|---	|
| CER-PRG-MIACT-00000  	| Unknown  	| 16 Sept 2022  	|
| CER-PRG-MIACT-00001  	| No Action found  	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00002  	| User aborted map  	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00003  	| Could not open map  	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00004  	| Could not read map  	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00005  	| Could not read inputs  	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00006  	| Invalid map handle  	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00007  	| Invalid card number was specified 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00008  	| One or more inputs was invalid 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00009  	| Target not available 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00010  	| Internal error 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00011  	| Could not build one or more outputs 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00012  	| Source not available 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00013  	| Could not open work files 	| 16 Sept 2022  	|
| CWG-ITX-IEXEC-00014  	| One or more outputs was invalid 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00015  	| Map must be recompiled 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00016  	| Disk write error 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00017  	| Disk read error 	| 16 Sept 2022  	|
| CWG-ITX-IEXEC-00018  	| Page usage count error 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00019  	| Internal calling error 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00020  	| Reopen file failed 	| 16 Sept 2022  	|
| CWG-ITX-IEXEC-00021  	| Input valid but unknown data found 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00022  	| Page size too small 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00023  	| Unable to reuse work file 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00024  	| Database error 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00025  	| File attribute error 	| 16 Sept 2022  	|
| CWG-ITX-IEXEC-00026  	| Output type in error 	| 16 Sept 2022  	|
| CWG-ITX-IEXEC-00027  	| Output type contains errors 	| 16 Sept 2022  	|
| CWG-ITX-IEXEC-00028  	| Input type contains errors 	| 16 Sept 2022  	|
| CWG-ITX-IEXEC-00029  	| Output valid, but unknown data found 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00030  	| FAIL function aborted map 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00032  	| Invalid map instance handle 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00033  	| Map instance handle in use 	| 16 Sept 2022  	|
| CWG-ITX-IEXEC-00034  	| Too few pages requested, more allocated 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00035  	| Insufficient number of pages to execute map 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00036  	| Could not open work files 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00037  	| Operation is not supported on the platform 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00050  	| Not enough memory to execute map 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00051  	| Card override failure 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00052  	| I/O initialization failure 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00053  	| Open audit failure 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00054  	| No command line 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00055  	| Recursive command files 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00056  	| Invalid command line option 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00057  	| Invalid `W' command line option 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00058  	| Invalid `B' command line option 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00059  	| Invalid `R' command line option 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00060  	| Invalid `A' command line option 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00061  	| Invalid `P' command line option 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00062  	| Invalid `Y' command line option 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00063  	| Invalid `T' command line option 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00064  	| Invalid `G' command line option 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00065  	| Invalid `I' command line option for input 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00066  	| Invalid size in echo command line for input 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00067  	| Invalid adapter type in command line for input 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00068  	| Invalid `O' command line option for output 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00069  	| Invalid adapter type in command line for output 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00070  	| Command line memory failure 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00071  	| Invalid `D' command line option 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00072  	| Invalid `F' command line option 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00073  	| Resource manager failure 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00074  	| Invalid `Z' command line option 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00075  	| Adapter failed to get data on input 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00076  	| Adapter failed to put data on output 	| 16 Sept 2022  	|
| CER-ITX-IEXEC-00077  	| Invalid map name 	| 16 Sept 2022  	|

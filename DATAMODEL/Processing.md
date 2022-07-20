# Processing #

[Home Page](../README.md)

## Getting Started ##
Le __Processing__ c'est le coeur de __FCT__. Il est né d'abord de ce qui était le __Brouteur__ dans __FCT__. Il a ensuite évolué avec les années afin d'arriver petit à petit à un __système complet__ de Processing.
Il y a une tendance à confondre le __Processing__ avec __FCT__, c'est normal car il contenait aussi à l'origine une fonctionnalité de __Matching__ qui a cependant été supprimé dans les évolutions pour implémenter un composant à part entière.
 
Le principe de base du __Processing__ est de pouvoir executer une ou plusieurs activités à la suite. D'un point de vue __ITX__, cela sera représenté par __l'execution d'une ou plusieurs maps__ où il sera possible d'échanger des données entre chacun d'entre elle.
> Ex: La réception d'un fichier EDIFACT transformé tout d'abord dans un format Pivot XML puis intégré dans un backend client


Le __second__ principe __important__ est de garder la possibilité de __réutilisabilité__ des activités et des scénario.
> Ex: Une activité d'encodage en Latin-1 disponible pour tous
> Ex: Un scénario d'intégration de fichier EDIFACT de type IFTMBF commun à tous client
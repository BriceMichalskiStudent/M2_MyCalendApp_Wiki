[MyCalendApp](./README.md)

# Bienvenue sur le [wiki MyCalendApp](https://mycalendapp.github.io/Wiki/) !

> [https://mycalendapp.herokuapp.com](https://mycalendapp.herokuapp.com)  
> [https://api-mycalendapp.herokuapp.com/](https://api-mycalendapp.herokuapp.com/)


## Introduction

MyCalendApp est un projet scolaire visant à mettre en place un réseau social. 
La particularité de ce réseau social est d'être orienté évènementiel local.
Cet application permettra aux utilisateurs de cree des événements et de les partagés simplement.
Les utilisateurs pourront cree des évènements public ou privé. 
L'application possède un certain nombre de fonctionalite : commentaires, inscription avec gestion de la liste de participants et un partage de photos ou videos sur les événements passés.


## Status

|          |      Backend      |  Frontend |
|----------|:-------------:|:------:|
|PROD|[![Website Prod](https://img.shields.io/website-up-down-green-red/http/api-mycalendapp.herokuapp.com/ping)](https://api-mycalendapp.herokuapp.com/ping)|[![Website Prod](https://img.shields.io/website-up-down-green-red/http/mycalendapp.herokuapp.com/)](https://mycalendapp.herokuapp.com)|


## Sommaire :

- [Specification](./specification/specification.md) 
    - [I - Spécification Globale](./specification/global.md)
    - [II - Spécification Détailée](./specification/detailed.md)
    - [III - User Story](./specification/user_stories.md)

- [Database](./database/database.md)
    - [Data Model](./database/model.md)
    - [MongoDB](./database/mongodb.md)
    
- [Graphisme](./graphisme/graphisme.md)
    - [Maquette](./graphisme/maquette.md)


## Intégration continue

|          |      Backend      |  Frontend |
|----------|:-------------:|:------:|
| develop | ![GitHub Super-Linter](https://github.com/MyCalendApp/backend/workflows/Continuous%20Integration/badge.svg?branch=develop)| ![GitHub Super-Linter](https://github.com/MyCalendApp/frontend/workflows/Continuous%20Integration/badge.svg?branch=develop) |
| master | ![GitHub Super-Linter](https://github.com/MyCalendApp/backend/workflows/Continuous%20Integration/badge.svg?branch=master)| ![GitHub Super-Linter](https://github.com/MyCalendApp/frontend/workflows/Continuous%20Integration/badge.svg?branch=master) |

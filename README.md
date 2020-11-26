[MyCalendApp](./README.md)

# Bienvenue sur le wiki MyCalendApp !

> [https://mycalendapp.herokuapp.com/profile](https://mycalendapp.herokuapp.com/profile)

## Introduction

MyCalendApp est un projet scolaire visant à mettre en place un réseau social. 
La particularité de ce réseau social est d'être orienté évènementiel local.
Cet application permettra aux utilisateurs de cree des événements et de les partagés simplement.
Les utilisateurs pourront cree des évènements public ou privé. 
L'application possède un certain nombre de fonctionalite : commentaires, inscription avec gestion de la liste de participants et un partage de photos ou videos sur les événements passés.



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

## Status

|          |      Backend      |  Frontend |
|----------|:-------------:|:------:|
|PROD|![Website Prod](https://img.shields.io/website-up-down-green-red/http/api-mycalendapp.herokuapp.com/ping)||
|DEV|![Website Dev](https://img.shields.io/website-up-down-green-red/http/dev-api-mycalendapp.herokuapp.com/ping)||

## Intégration continue


|          |      Backend      |  Frontend |
|----------|:-------------:|:------:|
| develop |  [![GitHub Super-Linter](https://github.com/MyCalendApp/backend/workflows/Continuous%20Integration/badge.svg?branch=develop)](https://dev-api-mycalendapp.herokuapp.com/ping) | ?? |
| master |   [![GitHub Super-Linter](https://github.com/MyCalendApp/backend/workflows/Continuous%20Integration/badge.svg?branch=master)](https://api-mycalendapp.herokuapp.com/ping)    | ?? |

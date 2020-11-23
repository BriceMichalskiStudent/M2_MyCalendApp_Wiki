[MyCalendApp](../README.md) > [Database](./database.md) > [MongoDB](./mongodb.md)

# MondoDB Page

## Cluster Information : 

> Cluster mongodb managé par [Mongo Atlas](https://www.mongodb.com/cloud/atlas)

### Hebergement

| Information | Value |  
|---|---|
| Provider  | AWS  |
| Zone | Frankfurt (eu-central-1)  |
| Replica Set | 3 nodes |

### Noeuds

| Node | Role |  
|---|---|
| mycalendapp-shard-00-00 | SECONDARY  |
| mycalendapp-shard-00-01 | PRIMARY  |
| mycalendapp-shard-00-02 | SECONDARY |

## Chaine de connection

`mongodb+srv://CalendAppUser:<secret>@mycalendapp.nbkps.mongodb.net/test`

## Base de données

- calendar_dev (pour le developpement et l'intégration)
- calendar_prod (pour l'environnement de production)

> La structure de base de données est accessible ici : [Data Model](./model.md)


[MyCalendApp](../README.md) > [Database](./database.md) > [MongoDB](./mongodb.md)

# MondoDB Page

## Cluster Information : 

> Cluster mongodb hebergé par [Mongo Atlas](https://www.mongodb.com/cloud/atlas)

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

## Connect String: 

> mongodb+srv://CalendAppUser:<secret>@mycalendapp.nbkps.mongodb.net/test

## Available database

- calendar_dev (for test and development)

- calendar_prod (for production environnement)


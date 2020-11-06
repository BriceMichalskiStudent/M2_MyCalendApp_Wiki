[MyCalendApp](../README.md) > [Spécification](./specification.md) > [Spécification Globale](./global.md)

# I - Spécification Globale

## 1 - Origine de besoin

Le projet MyCalendApp répond au besoin d'organisation, de découverte et de gestion d'événements en ligne. L'orientation calendrier de ce projet lui permettra de regrouper sur une seule page les événements à venir, d'accepter, de refuser ou d'envoyer des invitations. Un chat lié à chaque événement permettra au participant de s'y organiser, ainsi que de visualiser toutes les informations liées à l'événement. 

## 2 - Glossaire

...


## 3 - Objectifs

### Objectif Général

L'objectif principal du projet MyCalendApp est de fournir une plateforme pour simplifier l'organisation d'événements. 
Ainsi que de permettre aux utilisateurs de mieux organiser leur temps.

### Objectif Fonctionnel

Chaque utilisateur devra pouvoir:
- Créer, modifier, supprimer, inviter, rendre public ou privé un événement
- Rejoindre, quitter, consulter la liste des événements publics ou privés auxquels il a été invité
- Ajout d'amis pour pouvoir consulter les événements publics auxquels ils participent.
- de discuter, d'accéder à des images et à des informations sur les événements auxquels il s'est inscrit


### Objectif Fonctionnel Secondaire

Chaque utilisateur devra pouvoir le faire :
- S'abonner aux balises et ainsi être tenu informé lors de la création d'événements contenant cette balise.
- L'utilisateur doit pouvoir se connecter via son compte facebook et voir ses événements facebook sur son calendrier MyCalendApp.

### Cibles
Seront visés par cette application :
- Une population jeune adepte des outils numériques en ligne
- Les personnes ayant un cercle d'amis plus large et qui ont des difficultés d'organisation
- Personnes âgées ayant des pertes de mémoire

## 4 - Qualité de service et Securité

### Disponibilité 

La disponibilité de cette application dépendra de la disponibilité du fournisseur cloud Heroku, voir [Heroku Status Page](https://status.heroku.com/).

### Securité

Toutes les connexions à l'application MyCalendApp seront effectuées via le protocole HTTPS. Une analyse de sécurité des dépendances est également mise en œuvre par github via [Dependabot](https://docs.github.com/en/free-pro-team@latest/github/managing-security-vulnerabilities/about-alerts-for-vulnerable-dependencies).

Les autorisations se feront via un JWT et la connexion se fera via un mot de passe crypté en base de données.

## 5 - Livraison

La livraison en production se fera automatiquement lors du merge dans master selon le GitFlow Workflow.
Elle peut également être effectuée à la demande par l'équipe de développement. 

L'application sera accessible sur [https://mycalendapp.herokuapp.com/](https://mycalendapp.herokuapp.com/)
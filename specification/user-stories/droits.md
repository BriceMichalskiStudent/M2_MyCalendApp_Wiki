[MyCalendApp](../../README.md) > [Spécification](../specification.md) > [User Story](../user_stories.md) > [Droits](droits.md)

# ID: 2 Name: Droits d'acces
## Description
**En tant que** administrateur **je veux pouvoir** maitriser l'ensemble des droits d'acces de l'application **Afin de** restreindre l'accès a certaines informations et fonctionnalités jugé inutile pour certain 'type' d'utilisateur. 

## Règles metiers
**1.** Il existera 3 roles différents : Administrateur, Animateur et Communicant

## Validation
### Scenario 1 : Acces interdit
**Lorsque** je suis connecter en temps qu'utilisateur 
**Alors** je ne peux pas acceder a certaine page du site
**Et donc** le serveur me renvoie vers une page d'erreur 403 : acces interdit

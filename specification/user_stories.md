[MyCalendApp](../README.md) > [Spécification](./specification.md) > [User Stories](./user_stories.md)

# III - User Stories

## Sommaire des User Stories:

* [Login](#1---login) 
* [Droits d'accès](#2---droits-daccès)
* [Logs](#3---logs)

## 1 - Login

### Description

**En tant que** administrateur **je veux pouvoir** maitriser l'ensemble des utilisateurs de l'application **Afin de** pouvoir limiter l'accès aux informations de l'application strictement qu’aux personnes concernées. 

### Règles metiers

**1.** le formulaire contiendra seulement un champ `email` et `mots de passe`

### Validation

* #### Scenario 1 : Formulaire

    **Lorsque** je clique sur le lien `connexion` du menu  
    **Alors** je tombe sur le formulaire de connexion a l'application

* #### Scenario 2 : Connexion, redirection

    **Lorsque** je rentre le bon combo `email` et `mots de passe`

    **Alors** je suis automatiquement rediriger vers la page d'accueil du dashboard 

* #### Scenario 3 : Connexion, erreur

    **Lorsque** je rentre un mauvais combo `email` et `mots de passe`

    **Alors** un message d'erreur apparait m'indiquant que mon mots de passe ou mon email n'est pas bon.

* #### Scenario 4 : Mauvaise adresse mail

    **Lorsque** je rentre une adresse email qui ne respecte pas le bon format  
    **Alors** je ne peux pas soumettre le formulaire et un message d'erreur m'indique que l'adresse mail rentrer n'est pas bonne

* #### Scenario 5 : Non connecter, redirection

    **Lorsque** j'essaie de me rendre directement sur la page d'accueil de l'application agenda sans etre connecter.  
    **Alors** je suis rediriger automatiquement vers le formulaire de connexion avec un message m'indiquant que je dois etre connecter afin d'accéder a cette page. 

* #### Scenario 6 : Page mots de passe oublie (facultatif)

    **Lorsque** je ne trouve plus mon mots de passe  
    **Alors** je peux me rendre sur la page `mots de passe oublie`

* #### Scenario 7 : Reinitialisation de mots de passe, email existant (facultatif)

    **Lorsque** je rentre mon adresse mail dans le formulaire de la page mots de passe oublie et que je le soummet (double verification => pop-up: etes vous sur de vouloir réinitialiser votre mots de passe ?)  
    **Alors** je suis rediriger une page ou il est indiquer le succes de l'operation et je recois un mail m'indiquant mon nouveau mots de passe

* #### Scenario 8 : Reinitialisation de mots de passe, email inconnu (facultatif)

    **Lorsque** je rentre mon adresse mail dans le formulaire de la page mots de passe oublie et que je le soummet (double verification => pop-up: etes vous sur de vouloir réinitialiser votre mots de passe ?)  
    **Alors** celui-ci m'afficher une page d'erreur m'indiquant qu'aucun utilisateur utilisant cet adresse email n'est connu.

## 2 - Droits d'accès

### Description

En tant que :

* #### Utilisateur anonyme

    **je veux pouvoir** : 

    - Consulter la liste des evenements à proximités ainsi que leurs details ainsi qu'aux commentaires liés à cet event. 
    - Je veux pouvoir avoir accés à un formulaire d'inscription. 

* #### Utilisateur authentifié

    En plus des droits des utilsateuranonymes, **je veux pouvoir** :

    - Je veux pouvoir me connecter avec mes identifiants.
    - Je veux pouvoir modifier/supprimer mon compte utilisateur.
    - M'inscrire / Me déinscrire à un des evenements à proximités
    - Ajouter des commentaires sous les evenements à proximités
    - Créer un évenement, acceder à la liste des participants, modifier l'evenements.

* #### administrateur

    En plus des droits des utilsateurs authentifiés, **je veux pouvoir** : 

    - Gerer les comptes utilistateurs (CRUD)
    - Gerer l'ensembles des evenements (CRUD)
    - Validée/Supprimer les commentaires detecté comme étant injurieux

### Règles metiers

**1.** Il existera 2 roles différents : Utilisateur, administrateur

### Validation

#### Scenario 1 : Acces interdit
**Lorsque** je suis connecter en temps qu'utilisateur 
**Alors** je ne peux pas acceder a certaine page du site
**Et donc** le serveur me renvoie vers une page d'erreur 403 : acces interdit

## 3 - logs

### Description
**En tant que** administrateur **je veux pouvoir** avoir une vue sur les logs de l'application **Afin de** connaîtres les derrieres actions faites avant l'éruption d'un bug ou autre. 

### Règles metiers

**1.** Seuls les administrateurs peuvent consulter les logs de l'application

### Validation

#### Scenario 1 : Consultation
**Lorsque que** je suis connecter a l'application en tant qu’administrateur
**Alors** je peux consulter la page log de l'application

#### Scenario 2 : Refus

**Lorsque** je suis connecter a l'application en tant que rédacteur
**Alors** je ne peux pas accéder a la page log (celle-ci ne figure pas dans le menu)

## 4 - Create an account

## 5 - Create Event

## 6 - Inscription

## 7 - Add Comments

## 8 - Management des participants

## 9 - Envoie email

## 10 - Gestion du compte

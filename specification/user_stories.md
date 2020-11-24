[MyCalendApp](../README.md) > [Spécification](./specification.md) > [User Stories](./user_stories.md)

# III - User Stories

- [Login](#1---login) 
- [Droits d'accès](#2---droits-daccès)
- [Create account](#3---create-an-account)
- [Create events](#4---create-event)
- [Event inscription](#5---event-inscription)
- [Comments](#6---comments)
- [Management des participants](#7---management-des-participants)
- [Send email](#8---send-email)
- [User account](#9---user-account)





## 1 - Login

### Description

Sont ici décrites, les regles et modalités de connexion, d'oublie, de reinitialisation de son mot de passe.

### Règles metiers

**1.** Lors de la connexion le formulaire contiendra seulement un champ `email` et `mots de passe`

**2.** Lors de l'inscription seront demandé les champs : `nom`,`prenom`,`genre`,`email`,`telephone`,`mots de passe`

### Validation

* #### Scenario 1 : Formulaire

    **Lorsque** je clique sur le lien `connexion` du menu  
    **Alors** je tombe sur le formulaire de connexion a l'application

* #### Scenario 2 : Connexion, redirection

    **Lorsque** je rentre le bon combo `email` et `mots de passe`

## 2 - Droits d'accès

### Description

En tant que :

* #### Utilisateur anonyme

    **je veux pouvoir** : 

    - Consulter la liste des événements  à proximités ainsi que leurs details ainsi qu'aux commentaires liés à cet event. 
    - Je veux pouvoir avoir accés à un formulaire d'inscription. 

* #### Utilisateur authentifié

    En plus des droits des utilsateuranonymes, **je veux pouvoir** :

    - Je veux pouvoir me connecter avec mes identifiants.
    - Je veux pouvoir modifier/supprimer mon compte utilisateur.
    - M'inscrire / Me déinscrire à un des événements  à proximités
    - Ajouter des commentaires sous les événements  à proximités
    - Créer un évenement, acceder à la liste des participants, modifier l'événements .

* #### administrateur

    En plus des droits des utilsateurs authentifiés, **je veux pouvoir** : 

    - Gerer les comptes utilistateurs (CRUD)
    - Gerer l'ensembles des événements  (CRUD)
    - Validée/Supprimer les commentaires detecté comme étant injurieux

### Règles metiers

1. Il existera 2 roles différents : Utilisateur, administrateur

### Validation

- #### Scenario 1 : Acces interdit

    **Lorsque** je suis connecter en temps qu'utilisateur  
    **Alors** je ne peux pas accéder a certaine page du site  
    **Et donc** le serveur me renvoie vers une page d'erreur 403 : acces interdit  


## 3 - Creation de compte

### Description

Sont ici décrites, les régles et modalités de connexion à L'application MyCalendApp

- #### Scenario 1 : Creation
    **Lorsque que** je visite le site  
    **Alors** je peux me cree un compte facilement grace un combo `adresse mail` et `mots de passe` 

- #### Scenario 2 : Consultation
    **Lorsque que** je suis connecter a l'application  
    **Alors** je peux consulter les pages mon comptes, mes inscriptions et mes évènements

- #### Scenario 3 : Securite
    **Lorsque** j'essaie de cree un compte avec une adresse email deja existante  
    **Alors** le site me renvoie une erreur : Cette adresse email est deja associer a un compte utilisateur.

### Validation

L'ensemble des fonctionnalités décrites ci-dessus sont implémentées


## 4 - Create Event

### Description

Sont ici décrites, les règles et modalités relatives à la création d'événements.

### Règles metiers
1. Seuls les utilisateurs authentifiés peuvent accéder à cette fonction

### Validation
- #### Scenario 1 : Formulaire
    **Lorsque que** je suis connecter a l'application  
    **Alors** je peux accéder et soumettre le formulaire de creation d'évènement

- #### Scenario 2 : Creation
    **Lorsque** je valide l'ensemble des informations du formulaire de creation d'évènement  
    **Alors** mon évènement est publie sur le site et est accessible.

## 5 - Event inscription
### Description

Sont ici décrites, les régles et modalités relatives à l'inscription aux événements.

### Règles metiers
1. Seuls les utilisateurs authentifiés peuvent accéder à cette fonction

### Validation
- #### Scenario 1 : Inscription
    **Lorsque que** je suis connecter a l'application et que je me rend sur une page detail d'un évènement  
    **Alors** je peux m'inscrire a cet évènement en cliquant sur un bouton

- #### Scenario 2 : Désinscription
    **Lorsque que** je suis connecter a l'application et que je me rend sur une page detail d'un évènement  
    **Alors** je peux me désinscrire de cet évènement en cliquant sur un bouton

- #### Scenario 3 : Mes inscriptions
**Lorsque que** je suis connecter a l'application
**Alors** je peux me rendre sur la page mes inscriptions, celle-ci reference l'ensemble des évènements auquel je me suis inscrit.

## 6 - Comments
### Description

Sont ici décrites, les régles et modalités relatives à l'envoie de commentaires sous un événement.

### Règles metiers
1. Seuls les utilisateurs authentifiés peuvent accéder à cette fonction

### Validation
- #### Scenario 1 : Formulaire
    **Lorsque que** je suis connecter a l'application  
    **Alors** je peux commenter sur l'ensemble des pages de detail des évènements

- #### Scenario 2 : Creation
    **Lorsque** je valide soumet le formulaire de creation de commentaire  
    **Alors** mon commentaire est publie sous la page de l'évènement concerner.

## 7 - Management des participants
### Description

Sont ici décrites, les régles et modalités relatives à la consultation des participants à un événement

### Règles metiers

1. Seuls les utilisateurs authentifiés peuvent accéder à cette fonction
2. Seuls l'organisateur de l'évènement peut accéder à cette fonction

### Validation

- #### Scenario 1 : Consultation
    **Lorsque que** je suis connecter a l'application  
    **Alors** je peux accéder et soumettre le formulaire de creation d'évènement

- #### Scenario 2 : Management
    **Lorsque** je suis sur la page de mon évènement  
    **Alors** je peux consulter la liste des participants de l'évènement.


## 8 - Notification par email
### Description

Sont ici décrites, les régles et modalités relatives à l'envoie de notification par mail
 
### Validation
- #### Scenario 1 : Inscription
    **Lorsque que** je m'inscrit a un évènement  
    **Alors** je recois un mail me confirmant mon inscription 

- #### Scenario 2 : Commentaire
    **Lorsque qu'** un utilisateur commente mon évènement
    **Alors** je recois un mail avec le contenu de son commentaire mon inscription

## 9 - Compte Utilisateur
### Description

Sont ici décrites, les régles et modalités relatives à la gestion de son compte utilisateur.

### Règles metiers
1. Seuls les utilisateurs authentifiés peuvent accéder à cette fonction

### Validation
- #### Scenario 1 : Modification
    **Lorsque que** je suis connecter  
    **Alors** j'ai accéder a la page `mon compte` qui me permet de modifier l'ensemble des informations de mon compte utilisateur.

- #### Scenario 2 : Suppression
    **Lorsque** je suis connecter  
    **Alors** j'ai accéder a la page `mon compte` qui me permet de supprimer de manière definitive mon compte.

- #### Scenario 3 : Portabilité (optionel)
    **Lorsque** je suis connecter  
    **Alors** j'ai accéder a la page `mon compte` qui me permet de télécharger l'ensemble de mes donnees.

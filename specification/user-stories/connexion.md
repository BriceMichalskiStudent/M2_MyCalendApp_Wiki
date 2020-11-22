[MyCalendApp](../../README.md) > [Spécification](../specification.md) > [User Story](../user_stories.md) > [Connexion](connexion.md)

# ID: 3 Name: Connexion
## Description
**En tant que** administrateur **je veux pouvoir** maitriser l'ensemble des utilisateurs de l'application **Afin de** pouvoir limiter l'accès aux informations de l'application strictement qu’aux personnes concernées. 

## Règles metiers
**1.** le formulaire contiendra seulement un champ `email` et `mots de passe`

## Validation
### Scenario 1 : Formulaire
**Lorsque** je clique sur le lien `connexion` du menu
**Alors** je tombe sur le formulaire de connexion a l'application
### Scenario 2 : Connexion, redirection
**Lorsque** je rentre le bon combo `email` et `mots de passe`
**Alors** je suis automatiquement rediriger vers la page d'accueil du dashboard 
### Scenario 3 : Connexion, erreur
**Lorsque** je rentre un mauvais combo `email` et `mots de passe`
**Alors** un message d'erreur apparait m'indiquant que mon mots de passe ou mon email n'est pas bon.
### Scenario 4 : Mauvaise adresse mail
**Lorsque** je rentre une adresse email qui ne respecte pas le bon format
**Alors** je ne peux pas soumettre le formulaire et un message d'erreur m'indique que l'adresse mail rentrer n'est pas bonne
### Scenario 5 : Non connecter, redirection
**Lorsque** j'essaie de me rendre directement sur la page d'accueil de l'application agenda (agenda.bm-lyon.fr/dashboard) sans etre connecter
**Alors** je suis rediriger automatiquement vers le formulaire de connexion avec un message m'indiquant que je dois etre connecter afin d'accéder a cette page 

### Scenario 6 : Page mots de passe oublie (facultatif)
**Lorsque** je ne trouve plus mon mots de passe
**Alors** je peux me rendre sur la page `mots de passe oublie`

### Scenario 7 : Reinitialisation de mots de passe, email existant (facultatif)
**Lorsque** je rentre mon adresse mail dans le formulaire de la page mots de passe oublie et que je le soummet (double verification => pop-up: etes vous sur de vouloir réinitialiser votre mots de passe ?) 
**Alors** je suis rediriger une page ou il est indiquer le succes de l'operation et je recois un mail m'indiquant mon nouveau mots de passe

### Scenario 8 : Reinitialisation de mots de passe, email inconnu (facultatif)
**Lorsque** je rentre mon adresse mail dans le formulaire de la page mots de passe oublie et que je le soummet (double verification => pop-up: etes vous sur de vouloir réinitialiser votre mots de passe ?) 
**Alors** celui-ci m'afficher une page d'erreur m'indiquant qu'aucun utilisateur utilisant cet adresse email n'est connu.

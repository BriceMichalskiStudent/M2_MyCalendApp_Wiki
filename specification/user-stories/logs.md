[MyCalendApp](../../README.md) > [Spécification](../specification.md) > [User Story](../user_stories.md) > [Logs](logs.md)

# ID: 1 Name: Logs
## Description
**En tant que** administrateur **je veux pouvoir** avoir une vue sur les logs de l'application **Afin de** connaîtres les derrieres actions faites avant l'éruption d'un bug ou autre. 

## Règles metiers
**1.** Seuls les administrateurs peuvent consulter les logs de l'application

## Validation
### Scenario 1 : Consultation
**Lorsque que** je suis connecter a l'application en tant qu’administrateur
**Alors** je peux consulter la page log de l'application
### Scenario 2 : Refus
**Lorsque** je suis connecter a l'application en tant que rédacteur
**Alors** je ne peux pas accéder a la page log (celle-ci ne figure pas dans le menu)

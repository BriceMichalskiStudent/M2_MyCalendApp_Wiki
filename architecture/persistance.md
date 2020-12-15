[MyCalendApp](../README.md) > [Architecture](./architecture.md) > [Persistance](./persistance.md)

# Persistance

## Base de données

Voir [ici](../database/mongodb.md)

## Persistance des images

Comme énnoncé sur la page concernant l'hergement, de part la gratuité et la nature meme du fonctionnement de Heroku, la persistance de fichier n'est pas possible sur cette plateforme.

La solution de contournements mise en place consiste à déléguer le stockage de nos images sur une instance [Amazon s3](https://aws.amazon.com/fr/s3/).

Le choix de cette solution c'est faite de part sa simplicité d'implémentation ainsi que part la présence d'une offre d'[essai gratuit](https://aws.amazon.com/fr/free/storage/) idéal pour un project etudiant.

**Un bucket aws s3 à donc été crée en voici les specifivités :**

> Region AWS : `UE (Paris) eu-west-3`

L'access en lecture seul a été ouvert au public afin de permettres l'affichage des images sur le front.

Pour les droits d'ecriture 2 utilisateurs ont été crées dans l'IAM (Identity and Access Management) Amazon. Chaqu'un donnant accès à un dossier specifique au environnement de dev et de prod.

Configuration des droit d'accès à notre bucket s3:

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicRead",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::mycalendapp-assets/*"
        },
        {
            "Sid": "AddCannedAcl",
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:iam::596721607746:user/mycalendapp-dev"
            },
            "Action": [
                "s3:PutObject",
                "s3:PutObjectAcl",
                "s3:DeleteObject"
            ],
            "Resource": "arn:aws:s3:::mycalendapp-assets/dev/*"
        },
        {
            "Sid": "AddCannedAcl",
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:iam::596721607746:user/mycalendapp-prod"
            },
            "Action": [
                "s3:PutObject",
                "s3:PutObjectAcl",
                "s3:DeleteObject"
            ],
            "Resource": "arn:aws:s3:::mycalendapp-assets/prod/*"
        }
    ]
}
```

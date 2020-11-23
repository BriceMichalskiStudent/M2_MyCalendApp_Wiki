[Home](../README.md) > [Database](./database.md) > [MongoDB](./model.md)

# Data Model

## User 

```json
{
    "name": {
        "title": "mr",
        "first": "brad",
        "last": "gibson"
    },
    "gender": "male",
    "mail": "test@test.com",
    "phone": "06 66 66 66 66",
    "password": "very_secret",
    "friends": [
      {"{User}": "{User}"}
    ],
    "tags": ["tag1","tag2"],
    "{Role}": "{Role}"
}
```

## Role 

Il y a 2 roles "ADMIN" et "USER".

```json
{
    "code": "ADMIN",
    "name": "Admin"
}
```

## Event 

```json
{
    "name": "Soirée D&D",
    "description": "Grosser soirée D&D",
    "dateEnd": "2020-11-24 2:00",
    "dateStart": "2020-11-23 21:00",
    "posts": [
        {"{Post}": "{Post}"}
    ],
    "creator": {
      "{User}": "{User}"
    }
}
```

## Post 

```json
{
    "message": "Salut trop cool cette soiré",
    "date": "2020-11-23 15:45",
    "upvote": 6,
    "downvote": 0,
    "creator": {
      "{User}": "{User}"
    }
}
```

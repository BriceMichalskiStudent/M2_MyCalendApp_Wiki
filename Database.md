hosting : Mongodb Atlas

### Connect: 

mongodb+srv://CalendAppUser:<secret>@mycalendapp.nbkps.mongodb.net/test

### Available database

- calendar_dev

- calendar_prod

# Data model

## users 

```json
{
    "gender": "male",
    "name": {
        "title": "mr",
        "first": "brad",
        "last": "gibson"
    },
    "password": "very_secret",
    "friends": ["ID1","ID2","..."],
    "tags": ["tag1","tag2"] 
}
```

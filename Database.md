# Mongodb Atlas

## Connect: 

mongodb+srv://CalendAppUser:<secret>@mycalendapp.nbkps.mongodb.net/test

## DB & Collection

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
    "location": {
        "street": "9278 new road",
        "city": "kilcoole",
        "state": "waterford",
        "postcode": "93027",
        "coordinates": {
            "latitude": "20.9267",
            "longitude": "-7.9310"
        },
        "timezone": {
            "offset": "-3:30",
            "description": "Newfoundland"
        }
    }
}
```

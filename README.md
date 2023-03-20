# restclient examples

```http
@id = 9223372036854775807
@baseUrl = https://petstore.swagger.io/v2/pet
```

```http
### Save a new pet

POST {{baseUrl}} HTTP/1.1
Content-Type: application/json
Accept: application/json

{

  "category": {
    "id": 0,
    "name": "fido rex"
  },
  "name": "doggie",
  "photoUrls": [
  ],
  "tags": [
    {
      "id": 0,
      "name": "growly"
    }
  ],
  "status": "available"
}
```

```http Update
### Update the pet

PUT {{baseUrl}}  HTTP/1.1
Content-Type: application/json
Accept: application/json

{
  "id": {{id}},
  "category": {
    "id": 0,
    "name": "fido"
  },
  "name": "fido rex .snr",
  "photoUrls": [
    "string"
  ],
  "tags": [
    {
      "id": 1,
      "name": "growly"
    }
  ],
  "status": "available"
}
```

```http
### Get the pet

GET {{baseUrl}}/{{id}} HTTP/1.1
```

```http Ger
### Get all pets

GET {{baseUrl}}/findByStatus?status=sold

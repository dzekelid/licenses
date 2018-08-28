{
  "info": {
    "name": "Flickr Photos Licenses Get Info",
    "_postman_id": "b065362f-5980-42be-a586-66d398d0a32b",
    "description": "Fetches a list of available photo licenses for Flickr.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Photos",
      "item": [
        {
          "id": "21819737-d8a3-4334-a5eb-268eb8ef8d3f",
          "name": "getRestMethodFlickr.photos.licenses.getinfo",
          "request": {
            "url": "http://api.flickr.com/services/rest/?method=flickr.photos.licenses.getInfo?api_key=%7B%7D&format=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Fetches a list of available photo licenses for Flickr."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4458fc8b-47d2-4712-bd31-34185edc9036"
            }
          ]
        }
      ]
    }
  ]
}
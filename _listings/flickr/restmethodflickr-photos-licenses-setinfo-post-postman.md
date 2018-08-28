{
  "info": {
    "name": "Flickr Photos Licenses Set Info",
    "_postman_id": "4050cf9a-c9f6-4df3-a232-db76547859a0",
    "description": "Sets the license for a photo.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Photos",
      "item": [
        {
          "id": "26890ef9-356f-4c3b-97f6-3f718e8ea4a0",
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
              "id": "00945756-9bb9-4391-94be-d7d81c9da9f8"
            }
          ]
        },
        {
          "id": "70107025-2b8e-4dca-b3e5-0634387b13e6",
          "name": "postRestMethodFlickr.photos.licenses.setinfo",
          "request": {
            "url": "http://api.flickr.com/services/rest/?method=flickr.photos.licenses.setInfo?api_key=%7B%7D&license_id=%7B%7D&photo_id=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Sets the license for a photo."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "67b7caff-dd84-48f4-b4d6-2b74b8e2d345"
            }
          ]
        }
      ]
    }
  ]
}
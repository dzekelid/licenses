{
  "info": {
    "name": "NetLicensing Licenses list",
    "_postman_id": "7b23d10b-3a21-433b-8e23-9ad70e533806",
    "description": "Return a list of all licenses for the current vendor",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "License",
      "item": [
        {
          "id": "4e873909-b3ff-43bf-bf9a-5aba305c6b6e",
          "name": "listLicenses",
          "request": {
            "url": "http://go.netlicensing.io/core/v2/rest/license",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Return a list of all licenses for the current vendor"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "308f784b-fda7-4fae-81ac-256a6f7deb6b"
            }
          ]
        }
      ]
    }
  ]
}
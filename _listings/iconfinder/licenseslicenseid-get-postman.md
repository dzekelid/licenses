{
  "info": {
    "name": "Icon Finder Get license details",
    "_postman_id": "9c8eb3fa-1fbf-4610-bbb5-b8559016cc0d",
    "description": "Get details about a specific license by its unique ID.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Licenses",
      "item": [
        {
          "id": "151cd789-3882-4a13-bb25-6c7da33c3b95",
          "name": "getLicensesLicense",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.iconfinder.com",
              "path": [
                "v2",
                "licenses/:licenseID"
              ],
              "variable": [
                {
                  "id": "licenseID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get details about a specific license by its unique ID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "06b13e8e-cca7-453e-9c9a-955b9610fcfa"
            }
          ]
        }
      ]
    }
  ]
}
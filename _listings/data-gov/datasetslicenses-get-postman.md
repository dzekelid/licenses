{
  "info": {
    "name": "Data.gov API Get Datasets Licenses",
    "_postman_id": "52bb7353-3adc-4aec-a3c9-5d0ee1a35ec5",
    "description": "List all available licenses",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "datasets",
      "item": [
        {
          "id": "b06ba288-30d7-4634-a8a6-6af6dd80ec81",
          "name": "getDatasetsLicenses",
          "request": {
            "url": "http://catalog.data.gov/api/3/datasets/licenses/",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List all available licenses"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "382a4d95-45a7-42ed-bebb-d5ab2a5b90e6"
            }
          ]
        }
      ]
    }
  ]
}
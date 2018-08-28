{
  "info": {
    "name": "NetLicensing Get licensee",
    "_postman_id": "1c158700-d7ec-46a7-9219-be5bcfbe18fc",
    "description": "Return a licensee by licenseeNumber",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "License",
      "item": [
        {
          "id": "15661f9f-6816-4a04-b6bd-977f07b2acc5",
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
              "id": "40d18e6b-61e9-4d79-9cbd-04d5bf546610"
            }
          ]
        },
        {
          "id": "5cf84b2d-e169-4b15-8b27-90eb74def050",
          "name": "createLicense",
          "request": {
            "url": "http://go.netlicensing.io/core/v2/rest/license",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "active",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "currency",
                  "value": "{}",
                  "disabled": false,
                  "description": "Specifies currency for the license price"
                },
                {
                  "key": "hidden",
                  "value": "{}",
                  "disabled": false,
                  "description": "If set to true, this license is not shown in NetLicensing Shop as purchased license"
                },
                {
                  "key": "licenseeNumber",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "licenseTemplateNumber",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Name for the licensed item"
                },
                {
                  "key": "number",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "parentfeature",
                  "value": "{}",
                  "disabled": false,
                  "description": "Mandatory for TIMEVOLUME license type and RENTAL licensing model"
                },
                {
                  "key": "price",
                  "value": "{}",
                  "disabled": false,
                  "description": "Price for the license"
                },
                {
                  "key": "startDate",
                  "value": "{}",
                  "disabled": false,
                  "description": "Mandatory for TIMEVOLUME license type"
                },
                {
                  "key": "timeVolume",
                  "value": "{}",
                  "disabled": false,
                  "description": "Mandatory for TIMEVOLUME license type"
                }
              ]
            },
            "description": "Creates a new license"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fceeb9a3-ca20-4452-9b1f-e75e4b9d5490"
            }
          ]
        },
        {
          "id": "f4cc39d6-bc1e-4415-b7d8-cb09c1db94a6",
          "name": "getLicense",
          "request": {
            "url": {
              "protocol": "http",
              "host": "go.netlicensing.io",
              "path": [
                "core",
                "v2",
                "rest",
                "license/:licenseNumber"
              ],
              "variable": [
                {
                  "id": "licenseNumber",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get license by a licenseNumber"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e3ba5ffb-f012-43b9-86f6-fabb28f9efd2"
            }
          ]
        },
        {
          "id": "8621d488-f681-4de2-9a3d-62bf2875315d",
          "name": "updateLicense",
          "request": {
            "url": {
              "protocol": "http",
              "host": "go.netlicensing.io",
              "path": [
                "core",
                "v2",
                "rest",
                "license/:licenseNumber"
              ],
              "variable": [
                {
                  "id": "licenseNumber",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "active",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "currency",
                  "value": "{}",
                  "disabled": false,
                  "description": "Specifies currency for the license price"
                },
                {
                  "key": "hidden",
                  "value": "{}",
                  "disabled": false,
                  "description": "If set to true, this license is not shown in NetLicensing Shop as purchased license"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Name for the licensed item"
                },
                {
                  "key": "number",
                  "value": "{}",
                  "disabled": false,
                  "description": "Unique number (across all products/licensees of a vendor) that identifies the license"
                },
                {
                  "key": "parentfeature",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "price",
                  "value": "{}",
                  "disabled": false,
                  "description": "Price for the license"
                },
                {
                  "key": "startDate",
                  "value": "{}",
                  "disabled": false,
                  "description": "for TIMEVOLUME licenseType"
                },
                {
                  "key": "timeVolume",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                }
              ]
            },
            "description": "Update license by a licenseNumber"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e3a48ae8-5814-40fe-96a2-07cfb44b9ef4"
            }
          ]
        },
        {
          "id": "a16be5ab-abea-449a-aa68-965974208389",
          "name": "deleteLicense",
          "request": {
            "url": {
              "protocol": "http",
              "host": "go.netlicensing.io",
              "path": [
                "core",
                "v2",
                "rest",
                "license/:licenseNumber"
              ],
              "variable": [
                {
                  "id": "licenseNumber",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete license by a licenseNumber"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "36cad8d1-bbee-4578-8a97-fd121fb3642b"
            }
          ]
        }
      ]
    },
    {
      "name": "Licensee",
      "item": [
        {
          "id": "90105bb8-3a92-4e9b-b555-d53a34a03ffa",
          "name": "listLicensees",
          "request": {
            "url": "http://go.netlicensing.io/core/v2/rest/licensee",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Return a list of all licensees for the current vendor"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "be208049-0d19-41a3-b41c-6e3821d15b76"
            }
          ]
        },
        {
          "id": "69e4ea3e-ec6a-4456-9e2d-b91402ddd0e8",
          "name": "createLicensee",
          "request": {
            "url": "http://go.netlicensing.io/core/v2/rest/licensee",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "active",
                  "value": "{}",
                  "disabled": false,
                  "description": "If set to false, the licensee is disabled"
                },
                {
                  "key": "licenseeSecret",
                  "value": "{}",
                  "disabled": false,
                  "description": "Licensee Secret for licensee"
                },
                {
                  "key": "markedForTransfer",
                  "value": "{}",
                  "disabled": false,
                  "description": "Mark licensee for transfer"
                },
                {
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "number",
                  "value": "{}",
                  "disabled": false,
                  "description": "Unique number (across all products of a vendor) that identifies the licensee"
                },
                {
                  "key": "productNumber",
                  "value": "{}",
                  "disabled": false,
                  "description": "productNumber to assign new licensee object"
                }
              ]
            },
            "description": "Creates a new licensee"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f9508923-cea3-4dac-a6ad-ce9489f6635f"
            }
          ]
        },
        {
          "id": "a267a278-8fff-4e21-a716-d50537882267",
          "name": "getLicensee",
          "request": {
            "url": {
              "protocol": "http",
              "host": "go.netlicensing.io",
              "path": [
                "core",
                "v2",
                "rest",
                "licensee/:licenseeNumber"
              ],
              "variable": [
                {
                  "id": "licenseeNumber",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Return a licensee by licenseeNumber"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "90d43ad1-6859-4a87-95a9-32eff2608ca6"
            }
          ]
        },
        {
          "id": "8d15aec7-2597-4522-b8b4-22003c32e124",
          "name": "deleteLicensee",
          "request": {
            "url": {
              "protocol": "http",
              "host": "go.netlicensing.io",
              "path": [
                "core",
                "v2",
                "rest",
                "licensee/:licenseeNumber"
              ],
              "query": [
                {
                  "key": "forceCascade",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "licenseeNumber",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete a licensee by number"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5ce00209-bf0d-4dff-9bc8-56f5ab557f29"
            }
          ]
        }
      ]
    }
  ]
}
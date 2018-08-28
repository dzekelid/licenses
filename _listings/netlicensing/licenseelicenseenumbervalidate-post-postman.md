{
  "info": {
    "name": "NetLicensing Validate licensee",
    "_postman_id": "4ec9a854-e30c-4f43-9b43-0735ba0da286",
    "description": "Validates active licenses of the licensee",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "License",
      "item": [
        {
          "id": "2f77a445-c178-4541-9a29-5dd6c80cbb4e",
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
              "id": "3bc04fd9-3f84-48a5-b6f0-466cfa5c4404"
            }
          ]
        },
        {
          "id": "0b553ff4-3c73-4526-9767-3c499d24610e",
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
              "id": "3c8a07b7-0985-4d46-b382-bce20319d1da"
            }
          ]
        },
        {
          "id": "2b22fcbb-26e4-4381-b4e1-2754af1d5680",
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
              "id": "1d4760c2-fe3a-44c9-81fa-68322ee1053e"
            }
          ]
        },
        {
          "id": "703b45ee-4041-47e0-a370-9f71b26061da",
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
              "id": "a56e2b37-00ae-4f85-b150-3f6ea36414b7"
            }
          ]
        },
        {
          "id": "0f5862bb-db52-4501-862b-c16248da880e",
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
              "id": "f75efba5-ff88-4e2d-ba09-a2e49fe722ae"
            }
          ]
        }
      ]
    },
    {
      "name": "Licensee",
      "item": [
        {
          "id": "c2e45dba-ca4d-448d-b1fe-eab6c2897235",
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
              "id": "fdfd816a-bdaf-47a5-8254-613a11a6d5f7"
            }
          ]
        },
        {
          "id": "4b54e284-deba-4065-aaeb-4829a55eaa6c",
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
              "id": "9b82b8f4-baee-4311-8181-9880adfe1185"
            }
          ]
        },
        {
          "id": "4729c5b7-a62e-46d3-9013-7937d89c4ccd",
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
              "id": "dc068b12-a762-4f77-9ea4-bb6ad71d5cb3"
            }
          ]
        },
        {
          "id": "c0f73f2c-4fab-4729-92ba-b1b07ae75b0d",
          "name": "updateLicensee",
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
                  "description": "New licensee number (update)"
                }
              ]
            },
            "description": "Sets the provided properties to a licensee. Return an updated licensee"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "44faae36-de7b-4743-bd62-e7ffaa1854e1"
            }
          ]
        },
        {
          "id": "f754e8a4-a450-4276-8a9f-2b55f63055a4",
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
              "id": "f26b7635-e81b-4564-9470-31dc9dc62d39"
            }
          ]
        },
        {
          "id": "e6bcdcf9-b599-47af-8376-c95d793d2a4a",
          "name": "transferLicenses",
          "request": {
            "url": {
              "protocol": "http",
              "host": "go.netlicensing.io",
              "path": [
                "core",
                "v2",
                "rest",
                "licensee/:licenseeNumber/transfer"
              ],
              "variable": [
                {
                  "id": "licenseeNumber",
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
                  "key": "sourceLicenseeNumber",
                  "value": "{}",
                  "disabled": false,
                  "description": "Licensee number which licenses to be transferred"
                }
              ]
            },
            "description": "Licenses transfer between licensees"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cb880695-2209-45da-82ae-3d0868489984"
            }
          ]
        },
        {
          "id": "bf4f4995-1ce6-419b-b74e-c53cfea26d13",
          "name": "validateLicensee",
          "request": {
            "url": {
              "protocol": "http",
              "host": "go.netlicensing.io",
              "path": [
                "core",
                "v2",
                "rest",
                "licensee/:licenseeNumber/validate"
              ],
              "variable": [
                {
                  "id": "licenseeNumber",
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
                  "key": "licenseeName",
                  "value": "{}",
                  "disabled": false,
                  "description": "Human-readable name for the auto-created licensee (will be set as custom Licensee property)"
                },
                {
                  "key": "licenseeSecret",
                  "value": "{}",
                  "disabled": false,
                  "description": "Licensee Secret key for licensee"
                },
                {
                  "key": "productNumber",
                  "value": "{}",
                  "disabled": false,
                  "description": "Product number, must be provided when licensee auto-create is enabled (see also Product JavaDoc)"
                }
              ]
            },
            "description": "Validates active licenses of the licensee"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b15ba56c-c0d3-47d6-87c5-2768c36769a3"
            }
          ]
        }
      ]
    }
  ]
}
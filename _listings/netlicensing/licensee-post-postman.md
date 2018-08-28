{
  "info": {
    "name": "NetLicensing Create licensee",
    "_postman_id": "a926c9fa-16ab-47a7-9ad1-9ea7ecb0918d",
    "description": "Creates a new licensee",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "License",
      "item": [
        {
          "id": "d58918d4-d4d2-4e26-8a68-25ab2e109a1a",
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
              "id": "81602428-2066-4e1d-bbf6-be53c2bf470e"
            }
          ]
        },
        {
          "id": "18840c0f-c762-48b5-9c58-c32e9d3e5989",
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
              "id": "48700b31-54bc-4637-93db-bb36db901dba"
            }
          ]
        },
        {
          "id": "4fe0d0d8-5fdf-47db-ba08-91dfe3a726c6",
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
              "id": "ad0e7c24-cbfd-44df-bdf8-566950f71d36"
            }
          ]
        },
        {
          "id": "2fcfd772-97dd-48e4-8457-d62808578b8a",
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
              "id": "239855d8-d039-450d-a3d7-cab1e303ab9c"
            }
          ]
        },
        {
          "id": "d11ec43c-a89d-466c-9597-71720de1eb44",
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
              "id": "88bd166d-1a19-4b29-892d-b2ddb8e92836"
            }
          ]
        }
      ]
    },
    {
      "name": "Licensee",
      "item": [
        {
          "id": "30153430-fd7d-4514-a185-89acac967706",
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
              "id": "8832c341-e111-42cd-974f-dae788643317"
            }
          ]
        },
        {
          "id": "36946e51-0804-416b-a05d-a2dce6490e9d",
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
              "id": "24dd29b8-aa88-4777-860e-4aaf95768d1a"
            }
          ]
        }
      ]
    }
  ]
}
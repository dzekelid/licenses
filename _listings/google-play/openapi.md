swagger: "2.0"
x-collection-name: Google Play
x-complete: 1
info:
  title: Google Play
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /enterprises/{enterpriseId}/groupLicenses:
    get:
      summary: Get Group Licenses
      description: Retrieves IDs of all products for which the enterprise has a group
        license.
      operationId: androidenterprise.grouplicenses.list
      x-api-path-slug: enterprisesenterpriseidgrouplicenses-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      responses:
        200:
          description: OK
      tags:
      - License
  /enterprises/{enterpriseId}/groupLicenses/{groupLicenseId}:
    get:
      summary: Get Group License
      description: Retrieves details of an enterprise's group license for a product.
      operationId: androidenterprise.grouplicenses.get
      x-api-path-slug: enterprisesenterpriseidgrouplicensesgrouplicenseid-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: groupLicenseId
        description: The ID of the product the group license is for, e
      responses:
        200:
          description: OK
      tags:
      - License
  /enterprises/{enterpriseId}/groupLicenses/{groupLicenseId}/users:
    get:
      summary: Get Group License User
      description: Retrieves the IDs of the users who have been granted entitlements
        under the license.
      operationId: androidenterprise.grouplicenseusers.list
      x-api-path-slug: enterprisesenterpriseidgrouplicensesgrouplicenseidusers-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: groupLicenseId
        description: The ID of the product the group license is for, e
      responses:
        200:
          description: OK
      tags:
      - License
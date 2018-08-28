---
swagger: "2.0"
x-collection-name: Google Play
x-complete: 0
info:
  title: Google Play Get Group License
  version: 1.0.0
  description: Retrieves details of an enterprise's group license for a product.
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
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---
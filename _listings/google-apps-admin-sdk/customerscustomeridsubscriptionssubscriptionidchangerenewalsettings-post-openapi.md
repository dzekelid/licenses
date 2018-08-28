---
swagger: "2.0"
x-collection-name: Google Apps Admin SDK
x-complete: 0
info:
  title: Google Apps Admin SDK API Update User License
  version: 1.0.0
  description: Update a user license's renewal settings. This is applicable for accounts
    with annual commitment plans only.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{productId}/sku/{skuId}/user:
    post:
      summary: Assign License
      description: Assign License.
      operationId: licensing.licenseAssignments.insert
      x-api-path-slug: productidskuskuiduser-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: productId
        description: Name for product
      - in: path
        name: skuId
        description: Name for sku
      responses:
        200:
          description: OK
      tags:
      - License
  /{productId}/sku/{skuId}/user/{userId}:
    delete:
      summary: Revoke License
      description: Revoke License.
      operationId: licensing.licenseAssignments.delete
      x-api-path-slug: productidskuskuiduseruserid-delete
      parameters:
      - in: path
        name: productId
        description: Name for product
      - in: path
        name: skuId
        description: Name for sku
      - in: path
        name: userId
        description: email id or unique Id of the user
      responses:
        200:
          description: OK
      tags:
      - License
    get:
      summary: Get License
      description: Get license assignment of a particular product and sku for a user
      operationId: licensing.licenseAssignments.get
      x-api-path-slug: productidskuskuiduseruserid-get
      parameters:
      - in: path
        name: productId
        description: Name for product
      - in: path
        name: skuId
        description: Name for sku
      - in: path
        name: userId
        description: email id or unique Id of the user
      responses:
        200:
          description: OK
      tags:
      - License
    patch:
      summary: Update License
      description: Assign License. This method supports patch semantics.
      operationId: licensing.licenseAssignments.patch
      x-api-path-slug: productidskuskuiduseruserid-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: productId
        description: Name for product
      - in: path
        name: skuId
        description: Name for sku for which license would be revoked
      - in: path
        name: userId
        description: email id or unique Id of the user
      responses:
        200:
          description: OK
      tags:
      - License
    put:
      summary: Update License
      description: Assign License.
      operationId: licensing.licenseAssignments.update
      x-api-path-slug: productidskuskuiduseruserid-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: productId
        description: Name for product
      - in: path
        name: skuId
        description: Name for sku for which license would be revoked
      - in: path
        name: userId
        description: email id or unique Id of the user
      responses:
        200:
          description: OK
      tags:
      - License
  /{productId}/sku/{skuId}/users:
    get:
      summary: Get License Assignment For Product
      description: List license assignments for given product and sku of the customer.
      operationId: licensing.licenseAssignments.listForProductAndSku
      x-api-path-slug: productidskuskuidusers-get
      parameters:
      - in: query
        name: customerId
        description: CustomerId represents the customer for whom licenseassignments
          are queried
      - in: query
        name: maxResults
        description: Maximum number of campaigns to return at one time
      - in: query
        name: pageToken
        description: Token to fetch the next page
      - in: path
        name: productId
        description: Name for product
      - in: path
        name: skuId
        description: Name for sku
      responses:
        200:
          description: OK
      tags:
      - License
  /{productId}/users:
    get:
      summary: Get License Assignment For User
      description: List license assignments for given product of the customer.
      operationId: licensing.licenseAssignments.listForProduct
      x-api-path-slug: productidusers-get
      parameters:
      - in: query
        name: customerId
        description: CustomerId represents the customer for whom licenseassignments
          are queried
      - in: query
        name: maxResults
        description: Maximum number of campaigns to return at one time
      - in: query
        name: pageToken
        description: Token to fetch the next page
      - in: path
        name: productId
        description: Name for product
      responses:
        200:
          description: OK
      tags:
      - License
  /customers/{customerId}/subscriptions/{subscriptionId}/changeRenewalSettings:
    post:
      summary: Update User License
      description: Update a user license's renewal settings. This is applicable for
        accounts with annual commitment plans only.
      operationId: reseller.subscriptions.changeRenewalSettings
      x-api-path-slug: customerscustomeridsubscriptionssubscriptionidchangerenewalsettings-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: customerId
        description: Either the customers primary domain name or the customers unique
          identifier
      - in: path
        name: subscriptionId
        description: This is a required property
      responses:
        200:
          description: OK
      tags:
      - License
  /customers/{customerId}/subscriptions/{subscriptionId}/changeSeats:
    post:
      summary: Update Suscription License
      description: Update a subscription's user license settings.
      operationId: reseller.subscriptions.changeSeats
      x-api-path-slug: customerscustomeridsubscriptionssubscriptionidchangeseats-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: customerId
        description: Either the customers primary domain name or the customers unique
          identifier
      - in: path
        name: subscriptionId
        description: This is a required property
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
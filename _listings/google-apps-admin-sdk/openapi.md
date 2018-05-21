---
swagger: "2.0"
x-collection-name: Google Apps Admin SDK
x-complete: 1
info:
  title: Google Apps Admin SDK Merged API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /customers/{customerId}/subscriptions/{subscriptionId}/suspend:
    post:
      summary: Suspect Subscription
      description: Suspends an active subscription.
      operationId: reseller.subscriptions.suspend
      x-api-path-slug: customerscustomeridsubscriptionssubscriptionidsuspend-post
      parameters:
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
      - LicenseSubscription
---
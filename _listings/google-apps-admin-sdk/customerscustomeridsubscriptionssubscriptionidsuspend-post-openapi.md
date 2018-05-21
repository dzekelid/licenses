---
swagger: "2.0"
x-collection-name: Google Apps Admin SDK
x-complete: 0
info:
  title: Google Apps Admin SDK API Suspect Subscription
  version: 1.0.0
  description: Suspends an active subscription.
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
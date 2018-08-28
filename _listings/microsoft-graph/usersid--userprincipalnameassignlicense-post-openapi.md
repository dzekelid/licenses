---
swagger: "2.0"
x-collection-name: Microsoft Graph
x-complete: 0
info:
  title: Microsoft Graph Assign License
  description: assignLicense Add or remove subscriptions for the user. You can also
    enable and disable specific plans associated with a subscription.
  version: 1.0.0
host: graph.microsoft.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/{id | userPrincipalName}/assignLicense:
    post:
      summary: Assign License
      description: assignLicense Add or remove subscriptions for the user. You can
        also enable and disable specific plans associated with a subscription.
      operationId: AssignLicense
      x-api-path-slug: usersid--userprincipalnameassignlicense-post
      parameters:
      - in: header
        name: Authorization
        description: 'Bearer '
      - in: header
        name: Content-Type
        description: application/json
      - in: path
        name: id | userPrincipalName
        type: string
      responses:
        200:
          description: OK
      tags:
      - Assign
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
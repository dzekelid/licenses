---
swagger: "2.0"
x-collection-name: CollabNet
x-complete: 0
info:
  title: CollabNet TeamForge API Documentation Gets alternative license types by userid.
  version: 1.0.0
  description: Gets alternative license types by userid..
basePath: /ctfrest/foundation/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/{userid}/alternative-licensetypes:
    get:
      summary: Gets alternative license types by userid.
      description: Gets alternative license types by userid..
      operationId: getLicenseById
      x-api-path-slug: usersuseridalternativelicensetypes-get
      parameters:
      - in: path
        name: userid
      responses:
        200:
          description: OK
      tags:
      - Alternative
      - License
      - Types
      - By
      - Userid
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
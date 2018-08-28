---
swagger: "2.0"
x-collection-name: CollabNet
x-complete: 0
info:
  title: CollabNet TeamForge API Documentation Gets valid license types
  version: 1.0.0
  description: Gets valid license types.
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
  /users/myself/alternative-licensetypes:
    get:
      summary: Gets alternative license types for current user.
      description: Gets alternative license types for current user..
      operationId: getLicenseForMyself
      x-api-path-slug: usersmyselfalternativelicensetypes-get
      responses:
        200:
          description: OK
      tags:
      - Alternative
      - License
      - Typescurrent
      - User
  /users/by-username/{username}/alternative-licensetypes:
    get:
      summary: Gets alternative license types by username.
      description: Gets alternative license types by username..
      operationId: getLicenseByUsername
      x-api-path-slug: usersbyusernameusernamealternativelicensetypes-get
      parameters:
      - in: path
        name: username
      responses:
        200:
          description: OK
      tags:
      - Alternative
      - License
      - Types
      - By
      - Username
  /server/licensetypes:
    get:
      summary: Gets valid license types
      description: Gets valid license types.
      operationId: getLicenseTypes
      x-api-path-slug: serverlicensetypes-get
      responses:
        200:
          description: OK
      tags:
      - Valid
      - License
      - Types
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
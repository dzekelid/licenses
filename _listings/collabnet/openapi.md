swagger: "2.0"
x-collection-name: CollabNet
x-complete: 1
info:
  title: Foundation API
  version: 1.0.0
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
  /server/licensekey:
    put:
      summary: Sets/Updates license key
      description: Sets/updates license key.
      operationId: enterLicenseKey
      x-api-path-slug: serverlicensekey-put
      parameters:
      - in: body
        name: body
        description: License key
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Sets
      - License
      - Key
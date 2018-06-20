---
swagger: "2.0"
x-collection-name: Iconfinder
x-complete: 1
info:
  title: Icon Finder
  description: give-your-users-instant-access-to-more-than-300000-icons-
  termsOfService: https://developer.iconfinder.com/api/2.0/terms.html
  version: v2
host: api.iconfinder.com
basePath: /v2/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /licenses/{licenseID}:
    get:
      summary: Get license details
      description: Get details about a specific license by its unique ID.
      operationId: getLicensesLicense
      x-api-path-slug: licenseslicenseid-get
      parameters:
      - in: path
        name: licenseID
        description: The unique id of the license
      responses:
        200:
          description: OK
      tags:
      - Licenses
---
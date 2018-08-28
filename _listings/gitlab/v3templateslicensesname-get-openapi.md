---
swagger: "2.0"
x-collection-name: GitLab
x-complete: 0
info:
  title: GitLab Get Templates Licenses Name
  version: 1.0.0
  description: This feature was introduced in GitLab 8.7.
host: localhost:3000
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/licenses:
    get:
      summary: Get Licenses
      description: This feature was introduced in GitLab 8.7. This endpoint is deprecated
        and will be removed in GitLab 9.0.
      operationId: getV3Licenses
      x-api-path-slug: v3licenses-get
      parameters:
      - in: query
        name: popular
        description: If passed, returns only popular licenses
      responses:
        200:
          description: OK
      tags:
      - Licenses
  /v3/licenses/{name}:
    get:
      summary: Get Licenses Name
      description: This feature was introduced in GitLab 8.7. This endpoint is deprecated
        and will be removed in GitLab 9.0.
      operationId: getV3LicensesName
      x-api-path-slug: v3licensesname-get
      parameters:
      - in: path
        name: name
        description: The name of the template
      responses:
        200:
          description: OK
      tags:
      - Licenses
      - Name
  /v3/templates/licenses:
    get:
      summary: Get Templates Licenses
      description: This feature was introduced in GitLab 8.7.
      operationId: getV3TemplatesLicenses
      x-api-path-slug: v3templateslicenses-get
      parameters:
      - in: query
        name: popular
        description: If passed, returns only popular licenses
      responses:
        200:
          description: OK
      tags:
      - Templates
      - Licenses
  /v3/templates/licenses/{name}:
    get:
      summary: Get Templates Licenses Name
      description: This feature was introduced in GitLab 8.7.
      operationId: getV3TemplatesLicensesName
      x-api-path-slug: v3templateslicensesname-get
      parameters:
      - in: path
        name: name
        description: The name of the template
      responses:
        200:
          description: OK
      tags:
      - Templates
      - Licenses
      - Name
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
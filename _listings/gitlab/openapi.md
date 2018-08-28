swagger: "2.0"
x-collection-name: GitLab
x-complete: 1
info:
  title: API title
  version: 1.0.0
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
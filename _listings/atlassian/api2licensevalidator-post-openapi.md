---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Cloud API Validate license
  description: |-
    Validates a Jira license.

    Typically used by the setup phase of the Jira application. Returns an object with a list of errors as key, value pairs if the license is not valid.
  termsOfService: http://atlassian.com/terms/
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/2/licenseValidator:
    post:
      summary: Validate license
      description: |-
        Validates a Jira license.

        Typically used by the setup phase of the Jira application. Returns an object with a list of errors as key, value pairs if the license is not valid.
      operationId: com.atlassian.jira.rest.v2.license.LicenceValidator.validateLicense_post
      x-api-path-slug: api2licensevalidator-post
      responses:
        200:
          description: OK
      tags:
      - Validate
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
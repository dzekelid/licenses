---
swagger: "2.0"
x-collection-name: Google Compute Engine
x-complete: 0
info:
  title: Google Compute Engine API Get License
  description: Returns the specified License resource. Get a list of available licenses
    by making a list() request.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: www.googleapis.com
basePath: /compute/v1/projects
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{project}/global/licenses/{license}:
    get:
      summary: Get License
      description: Returns the specified License resource. Get a list of available
        licenses by making a list() request.
      operationId: compute.licenses.get
      x-api-path-slug: projectgloballicenseslicense-get
      parameters:
      - in: path
        name: license
        description: Name of the License resource to return
      - in: path
        name: project
        description: Project ID for this request
      responses:
        200:
          description: OK
      tags:
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
swagger: "2.0"
x-collection-name: Google Compute Engine
x-complete: 1
info:
  title: Compute Engine
  description: creates-and-runs-virtual-machines-on-google-cloud-platform-
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
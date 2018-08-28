swagger: "2.0"
x-collection-name: Mattermost
x-complete: 1
info:
  title: Mattermost
  version: 1.0.0
host: your-mattermost-url.com
basePath: /api/v4
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /license:
    post:
      summary: Upload license file
      description: |-
        Upload a license to enable enterprise features.

        __Minimum server version__: 4.0

        ##### Permissions
        Must have `manage_system` permission.
      operationId: upload-a-license-to-enable-enterprise-features-minimum-server-version--40-permissionsmust-have-manag
      x-api-path-slug: license-post
      parameters:
      - in: formData
        name: license
        description: The license to be uploaded
      responses:
        200:
          description: OK
      tags:
      - Upload
      - License
      - File
    delete:
      summary: Remove license file
      description: |-
        Remove the license file from the server. This will disable all enterprise features.

        __Minimum server version__: 4.0

        ##### Permissions
        Must have `manage_system` permission.
      operationId: remove-the-license-file-from-the-server-this-will-disable-all-enterprise-features-minimum-server-ver
      x-api-path-slug: license-delete
      responses:
        200:
          description: OK
      tags:
      - Remove
      - License
      - File
  /license/client:
    get:
      summary: Get client license
      description: |-
        Get a subset of the server license needed by the client.
        ##### Permissions
        No permission required but having the `manage_system` permission returns more information.
      operationId: get-a-subset-of-the-server-license-needed-by-the-client-permissionsno-permission-required-but-having
      x-api-path-slug: licenseclient-get
      parameters:
      - in: query
        name: format
        description: Must be `old`, other formats not implemented yet
      responses:
        200:
          description: OK
      tags:
      - Client
      - License
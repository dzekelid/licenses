swagger: "2.0"
x-collection-name: Instructure
x-complete: 1
info:
  title: Instructure Canvas Utility APIs
  description: canvas-lms-includes-a-rest-api-for-accessing-and-modifying-data-externally-from-the-main-application-in-your-own-programs-and-scripts--
  termsOfService: https://www.canvaslms.com/policies/api-policy
  version: v1
host: canvas.instructure.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /courses/{course_id}/content_licenses:
    get:
      summary: List licenses
      description: List licenses.
      operationId: list-licenses
      x-api-path-slug: coursescourse-idcontent-licenses-get
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Content
      - Licenses
  /groups/{group_id}/content_licenses:
    get:
      summary: List licenses
      description: List licenses.
      operationId: list-licenses
      x-api-path-slug: groupsgroup-idcontent-licenses-get
      responses:
        200:
          description: OK
      tags:
      - Groups
      - Group
      - Id
      - Content
      - Licenses
  /users/{user_id}/content_licenses:
    get:
      summary: List licenses
      description: List licenses.
      operationId: list-licenses
      x-api-path-slug: usersuser-idcontent-licenses-get
      responses:
        200:
          description: OK
      tags:
      - Users
      - User
      - Id
      - Content
      - Licenses
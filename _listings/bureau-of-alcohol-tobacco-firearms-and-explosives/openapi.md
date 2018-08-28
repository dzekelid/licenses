swagger: "2.0"
x-collection-name: Bureau of Alcohol, Tobacco, Firearms, and Explosives
x-complete: 1
info:
  title: Bureau of Alcohol, Tobacco, Firearms, and Explosives
  version: 1.0.0
host: data.atf.gov
basePath: /resource/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  actions-on-federal-firearms-license-applications.json:
    get:
      summary: Actions On Federal Firearms License Applications
      description: Actions On Federal Firearms License Applications
      operationId: getActionsOnFederalFirearmsLicenseApplications.json
      x-api-path-slug: actionsonfederalfirearmslicenseapplications-json-get
      parameters:
      - in: query
        name: applications_abandoned
      - in: query
        name: applications_denied
      - in: query
        name: applications_withdrawn
      - in: query
        name: fiscal_year
      - in: query
        name: original_applications_processed
      responses:
        200:
          description: OK
      tags:
      - Actions
      - "On"
      - Federal
      - Firearms
      - License
      - Applications
      - Json
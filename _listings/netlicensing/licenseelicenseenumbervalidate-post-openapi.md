---
swagger: "2.0"
x-collection-name: NetLicensing
x-complete: 0
info:
  title: NetLicensing Validate licensee
  description: Validates active licenses of the licensee
  termsOfService: https://www.labs64.com/legal/terms-of-service/netlicensing
  version: 2.x
host: go.netlicensing.io
basePath: /core/v2/rest
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /license:
    get:
      summary: Licenses list
      description: Return a list of all licenses for the current vendor
      operationId: listLicenses
      x-api-path-slug: license-get
      responses:
        200:
          description: OK
      tags:
      - License
    post:
      summary: Create license
      description: Creates a new license
      operationId: createLicense
      x-api-path-slug: license-post
      parameters:
      - in: formData
        name: active
      - in: formData
        name: currency
        description: Specifies currency for the license price
      - in: formData
        name: hidden
        description: If set to true, this license is not shown in NetLicensing Shop
          as purchased license
      - in: formData
        name: licenseeNumber
      - in: formData
        name: licenseTemplateNumber
      - in: formData
        name: name
        description: Name for the licensed item
      - in: formData
        name: number
      - in: formData
        name: parentfeature
        description: Mandatory for TIMEVOLUME license type and RENTAL licensing model
      - in: formData
        name: price
        description: Price for the license
      - in: formData
        name: startDate
        description: Mandatory for TIMEVOLUME license type
      - in: formData
        name: timeVolume
        description: Mandatory for TIMEVOLUME license type
      responses:
        200:
          description: OK
      tags:
      - License
  /license/{licenseNumber}:
    delete:
      summary: Delete license
      description: Delete license by a licenseNumber
      operationId: deleteLicense
      x-api-path-slug: licenselicensenumber-delete
      parameters:
      - in: path
        name: licenseNumber
        description: Unique number (across all products/licensees of a vendor) that
          identifies the license
      responses:
        200:
          description: OK
      tags:
      - License
      - LicenseNumber
    get:
      summary: Get license
      description: Get license by a licenseNumber
      operationId: getLicense
      x-api-path-slug: licenselicensenumber-get
      parameters:
      - in: path
        name: licenseNumber
        description: Unique number (across all products/licensees of a vendor) that
          identifies the license
      responses:
        200:
          description: OK
      tags:
      - License
      - LicenseNumber
    post:
      summary: Update license
      description: Update license by a licenseNumber
      operationId: updateLicense
      x-api-path-slug: licenselicensenumber-post
      parameters:
      - in: formData
        name: active
      - in: formData
        name: currency
        description: Specifies currency for the license price
      - in: formData
        name: hidden
        description: If set to true, this license is not shown in NetLicensing Shop
          as purchased license
      - in: path
        name: licenseNumber
        description: Unique number (across all products/licensees of a vendor) that
          identifies the license
      - in: formData
        name: name
        description: Name for the licensed item
      - in: formData
        name: number
        description: Unique number (across all products/licensees of a vendor) that
          identifies the license
      - in: formData
        name: parentfeature
      - in: formData
        name: price
        description: Price for the license
      - in: formData
        name: startDate
        description: for TIMEVOLUME licenseType
      - in: formData
        name: timeVolume
      responses:
        200:
          description: OK
      tags:
      - License
      - LicenseNumber
  /licensee:
    get:
      summary: Licensees list
      description: Return a list of all licensees for the current vendor
      operationId: listLicensees
      x-api-path-slug: licensee-get
      responses:
        200:
          description: OK
      tags:
      - Licensee
    post:
      summary: Create licensee
      description: Creates a new licensee
      operationId: createLicensee
      x-api-path-slug: licensee-post
      parameters:
      - in: formData
        name: active
        description: If set to false, the licensee is disabled
      - in: formData
        name: licenseeSecret
        description: Licensee Secret for licensee
      - in: formData
        name: markedForTransfer
        description: Mark licensee for transfer
      - in: formData
        name: name
      - in: formData
        name: number
        description: Unique number (across all products of a vendor) that identifies
          the licensee
      - in: formData
        name: productNumber
        description: productNumber to assign new licensee object
      responses:
        200:
          description: OK
      tags:
      - Licensee
  /licensee/{licenseeNumber}:
    delete:
      summary: Delete licensee
      description: Delete a licensee by number
      operationId: deleteLicensee
      x-api-path-slug: licenseelicenseenumber-delete
      parameters:
      - in: query
        name: forceCascade
        description: Force object deletion and all descendants
      - in: path
        name: licenseeNumber
        description: Unique number (across all products of a vendor) that identifies
          the licensee
      responses:
        200:
          description: OK
      tags:
      - Licensee
      - LicenseeNumber
    get:
      summary: Get licensee
      description: Return a licensee by licenseeNumber
      operationId: getLicensee
      x-api-path-slug: licenseelicenseenumber-get
      parameters:
      - in: path
        name: licenseeNumber
        description: Unique number (across all products of a vendor) that identifies
          the licensee
      responses:
        200:
          description: OK
      tags:
      - Licensee
      - LicenseeNumber
    post:
      summary: Update licensee
      description: Sets the provided properties to a licensee. Return an updated licensee
      operationId: updateLicensee
      x-api-path-slug: licenseelicenseenumber-post
      parameters:
      - in: formData
        name: active
        description: If set to false, the licensee is disabled
      - in: path
        name: licenseeNumber
        description: Unique number (across all products of a vendor) that identifies
          the licensee
      - in: formData
        name: licenseeSecret
        description: Licensee Secret for licensee
      - in: formData
        name: markedForTransfer
        description: Mark licensee for transfer
      - in: formData
        name: name
      - in: formData
        name: number
        description: New licensee number (update)
      responses:
        200:
          description: OK
      tags:
      - Licensee
      - LicenseeNumber
  /licensee/{licenseeNumber}/transfer:
    post:
      summary: Transfer licenses
      description: Licenses transfer between licensees
      operationId: transferLicenses
      x-api-path-slug: licenseelicenseenumbertransfer-post
      parameters:
      - in: path
        name: licenseeNumber
        description: Licensee number with a maximum length of 1000 characters
      - in: formData
        name: sourceLicenseeNumber
        description: Licensee number which licenses to be transferred
      responses:
        200:
          description: OK
      tags:
      - Licensee
      - LicenseeNumber
      - Transfer
  /licensee/{licenseeNumber}/validate:
    post:
      summary: Validate licensee
      description: Validates active licenses of the licensee
      operationId: validateLicensee
      x-api-path-slug: licenseelicenseenumbervalidate-post
      parameters:
      - in: formData
        name: licenseeName
        description: Human-readable name for the auto-created licensee (will be set
          as custom Licensee property)
      - in: path
        name: licenseeNumber
        description: Licensee number with a maximum length of 1000 characters
      - in: formData
        name: licenseeSecret
        description: Licensee Secret key for licensee
      - in: formData
        name: productNumber
        description: Product number, must be provided when licensee auto-create is
          enabled (see also Product JavaDoc)
      responses:
        200:
          description: OK
      tags:
      - Licensee
      - LicenseeNumber
      - Validate
    get:
      summary: Validate licensee
      description: Validates active licenses of the licensee
      operationId: validateLicensee
      x-api-path-slug: licenseelicenseenumbervalidate-get
      parameters:
      - in: query
        name: licenseeName
        description: Human-readable name for the auto-created licensee (will be set
          as custom Licensee property)
      - in: path
        name: licenseeNumber
        description: Licensee number with a maximum length of 1000 characters
      - in: query
        name: productNumber
        description: Product number, must be provided when licensee auto-create is
          enabled (see also Product JavaDoc)
      responses:
        200:
          description: OK
      tags:
      - Licensee
      - LicenseeNumber
      - Validate
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
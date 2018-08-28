---
swagger: "2.0"
x-collection-name: Data.Gov
x-complete: 1
info:
  title: Data.gov API
  description: the-datagov-catalog-is-powered-by-ckan-a-powerful-open-source-data-platform-that-includes-a-robust-api-please-be-aware-that-datagov-and-the-datagov-ckan-api-only-contain-metadata-about-datasets-this-metadata-includes-urls-and-descriptions-of-datasets-but-it-does-not-include-the-actual-data-within-each-dataset
  version: "3"
host: catalog.data.gov
basePath: /api/3/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /datasets/licenses/:
    get:
      summary: Get Datasets Licenses
      description: List all available licenses
      operationId: getDatasetsLicenses
      x-api-path-slug: datasetslicenses-get
      responses:
        200:
          description: OK
      tags:
      - Datasets
      - Licenses
---
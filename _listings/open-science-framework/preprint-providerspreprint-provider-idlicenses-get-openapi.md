---
swagger: "2.0"
x-collection-name: Open Science Framework
x-complete: 0
info:
  title: Open Science Framework List all licenses
  description: |-
    A paginated list of the licenses allowed bya preprint provider.
    #### Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of 10 preprint providers. Each resource in the array is a separate preprint provider object.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  contact:
    name: OSF
    url: https://osf.io/support
    email: support@osf.io
  version: "2.0"
host: test-api.osf.io
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /licenses/:
    get:
      summary: List all licenses
      description: |-
        A paginated list of licenses. The returned licenses are sorted by their name.
        #### Returns
        Returns a JSON object containing `data` and `links` keys.
        The `data` key contains an array of 10 licenses. Each resource in the array is a separate license object and contains the full representation of the license, meaning additional requests to a license's detail view are not necessary.

        The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).

        This request should never return an error.
        #### Filtering
        You can optionally request that the response only include licenses that match your filters by utilizing the `filter` query parameter, e.g. [https://api.osf.io/v2/licenses/?filter[name]=apache](https://api.osf.io/v2/licenses/?filter[name]=apache).

        Licenses may be filtered by their `id`, and `name`.
      operationId: license_list
      x-api-path-slug: licenses-get
      responses:
        200:
          description: OK
      tags:
      - Licenses
  /preprint_providers/{preprint_provider_id}/licenses/:
    get:
      summary: List all licenses
      description: |-
        A paginated list of the licenses allowed bya preprint provider.
        #### Returns
        Returns a JSON object containing `data` and `links` keys.

        The `data` key contains an array of 10 preprint providers. Each resource in the array is a separate preprint provider object.

        The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).

        If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
      operationId: preprint_provider_licenses_list
      x-api-path-slug: preprint-providerspreprint-provider-idlicenses-get
      parameters:
      - in: path
        name: preprint_provider_id
        description: The unique identifier of the preprint provider
      responses:
        200:
          description: OK
      tags:
      - Preprint
      - Providers
      - Preprint
      - Provider
      - Licenses
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
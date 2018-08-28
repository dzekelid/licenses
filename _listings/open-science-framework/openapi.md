swagger: "2.0"
x-collection-name: Open Science Framework
x-complete: 1
info:
  title: Open Science Framework
  description: osf-provides-free-and-open-source-project-management-support-for-researchers-across-the-entire-research-lifecycle--as-a-collaboration-tool-osf-helps-researchers-work-on-projects-privately-with-a-limited-number-of-collaborators-and-make-parts-of-their-projects-public-or-make-all-the-project-publicly-accessible-for-broader-dissemination--as-a-workflow-system-osf-enables-connections-to-the-many-services-researchers-already-use-to-streamline-their-process-and-increase-efficiency--as-a-flexible-repository-it-can-store-and-archive-research-data-protocols-and-materials--
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
  /license/{license_id}/:
    get:
      summary: Retrieve a license
      description: |-
        Retrieves the details of a license.
        #### Returns
        Returns a JSON object with a `data` key containing the representation of the requested license, if the request is successful.

        If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
      operationId: licenses_read
      x-api-path-slug: licenselicense-id-get
      parameters:
      - in: path
        name: license_id
        description: The unique identifier of the license
      responses:
        200:
          description: OK
      tags:
      - License
      - License
  /:
    get:
      summary: Root
      description: |-
        Welcome to the Open Science Framework API. With this API you can access users, projects, components, logs, and files from the [Open Science Framework](https://osf.io/). The Open Science Framework (OSF) is a free, open-source service maintained by the [Center for Open Science](http://cos.io/).

        #### Returns
        A JSON object with `meta` and `links` keys.

        The `meta` key contains information such as a welcome message from the API, the specified version of the request, and the full representation of the current user, if authentication credentials were provided in the request.

        The `links` key contains links to the following entity collections: [addons](), [collections](), [institutions](#Institutions_institutions_list), [licenses](#Licenses_license_list), [metaschemas](), [nodes](#Nodes_nodes_list), [registrations](), [users](#Users_users_list)
      operationId: base_read
      x-api-path-slug: get
      responses:
        200:
          description: OK
      tags:
      - Root
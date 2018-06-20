---
name: Open Science Framework
x-slug: open-science-framework
description: OSF provides free and open source project management support for researchers
  across the entire research lifecycle. As a collaboration tool, OSF helps researchers
  work on projects privately with a limited number of collaborators and make parts
  of their projects public, or make all the project publicly accessible for broader
  dissemination. As a workflow system, OSF enables connections to the many services
  researchers already use to streamline their process and increase efficiency. As
  a flexible repository, it can store and archive research data, protocols, and materials.
image: ""
x-kinRank: "7"
x-alexaRank: "0"
tags: Licenses
created: "2018-06-20"
modified: "2018-06-20"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/licenses/master/_listings/open-science-framework/apis.md
specificationVersion: "0.14"
apis:
- name: Open Science Framework List all licenses
  x-api-slug: open-science-framework
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
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//licenses/
  tags: Licenses
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/licenses/master/_listings/open-science-framework/licenses-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/licenses/master/_listings/open-science-framework/licenses-get-openapi.md
- name: Open Science Framework List all licenses
  x-api-slug: open-science-framework
  description: |-
    A paginated list of the licenses allowed bya preprint provider.
    #### Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of 10 preprint providers. Each resource in the array is a separate preprint provider object.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//preprint_providers/{preprint_provider_id}/licenses/
  tags: Preprint,Providers,Preprint,Provider,Licenses
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/licenses/master/_listings/open-science-framework/preprint-providerspreprint-provider-idlicenses-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/licenses/master/_listings/open-science-framework/preprint-providerspreprint-provider-idlicenses-get-openapi.md
- name: Open Science Framework
  x-api-slug: open-science-framework
  description: OSF provides free and open source project management support for researchers
    across the entire research lifecycle. As a collaboration tool, OSF helps researchers
    work on projects privately with a limited number of collaborators and make parts
    of their projects public, or make all the project publicly accessible for broader
    dissemination. As a workflow system, OSF enables connections to the many services
    researchers already use to streamline their process and increase efficiency. As
    a flexible repository, it can store and archive research data, protocols, and
    materials.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2
  tags: Licenses
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/licenses/master/_listings/open-science-framework/openapi.md
x-common:
- type: x-website
  url: https://cos.io
- type: x-github
  url: https://github.com/OSFramework
- type: x-twitter
  url: https://twitter.com/OSFramework
- type: x-website
  url: http://osf.io
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---
---
name: Google Apps Admin SDK
x-slug: google-apps-admin-sdk
description: Administer domain resources, create reports, and manage subscriptions.
  Use the Directory API to create and manage users and groups for a domain, along
  with their aliases. Programmatically access the functionality found at the Admin
  console Organization and users tab. Use the Reports API to gain insights on content
  management with Google Drive activity reports. Audit administrator actions. Generate
  customer and user usage reports.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/nexusae0_icon2.png
x-kinRank: "9"
x-alexaRank: "0"
tags: Licenses
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/licenses/master/_listings/google-apps-admin-sdk/apis.md
specificationVersion: "0.14"
apis:
- name: Google Apps Admin SDK API Suspect Subscription
  x-api-slug: google-apps-admin-sdk-api
  description: Suspends an active subscription.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/nexusae0_icon2.png
  humanURL: https://developers.google.com/admin-sdk/
  baseURL: https://///customers/{customerId}/subscriptions/{subscriptionId}/suspend
  tags: LicenseSubscription
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/licenses/master/_listings/google-apps-admin-sdk/customerscustomeridsubscriptionssubscriptionidsuspend-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/licenses/master/_listings/google-apps-admin-sdk/customerscustomeridsubscriptionssubscriptionidsuspend-post-openapi.md
- name: Google Apps Admin SDK API
  x-api-slug: google-apps-admin-sdk-api
  description: Administer domain resources, create reports, and manage subscriptions.
    Use the Directory API to create and manage users and groups for a domain, along
    with their aliases. Programmatically access the functionality found at the Admin
    console Organization and users tab. Use the Reports API to gain insights on content
    management with Google Drive activity reports. Audit administrator actions. Generate
    customer and user usage reports.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/nexusae0_icon2.png
  humanURL: https://developers.google.com/admin-sdk/
  baseURL: https:///
  tags: Licenses
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/licenses/master/_listings/google-apps-admin-sdk/openapi.md
x-common:
- type: x-blog
  url: https://gsuite-developers.googleblog.com/search/label/Admin%20SDK
- type: x-blog-rss
  url: https://gsuite-developers.googleblog.com/feeds/posts/default?alt=rss
- type: x-issues
  url: https://code.google.com/a/google.com/p/apps-api-issues/issues/list?q=label:API-Apps
- type: x-website
  url: https://developers.google.com/admin-sdk/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---
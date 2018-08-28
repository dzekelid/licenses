swagger: "2.0"
x-collection-name: Cisco WebEx
x-complete: 1
info:
  title: Webex Teams API
  description: hey-there-thanks-for-checking-out-cisco-webex-for-developers--if-youve-used-cisco-webex-meetings-or-cisco-webex-teams-formerly-cisco-spark-you-know-how-easy-it-is-to-meet-and-collaborate-with-your-team-members-and-customers-the-webex-for-developers-program-opens-up-the-power-behind-the-webex-platform-to-anyone-seeking-to-extend-the-webex-experience-webex-meetings-is-a-powerful-conferencing-solution-that-lets-you-connect-with-anyone-anywhere-in-real-time--by-combining-video-audio-and-content-sharing-webex-meetings-creates-an-effective-conferencing-environment-leading-to-more-productive-meetings-and-increased-productivity--developer-information-for-webex-meetings-will-soon-be-available-on-this-site--in-the-meantime-to-get-started-with-developing-for-webex-meetings-please-see-the-getting-started-guides-over-on-cisco-devnet--keep-reading-for-information-about-webex-teams-webex-teams-makes-staying-in-sync-with-your-teammates-and-customers-easy-conversations-in-webex-teams-take-place-in-virtual-meeting-rooms--some-rooms-live-for-a-few-hours-while-others-become-permanent-fixtures-of-your-teams-workflow-with-titles-like-daily-standup-or-build-status--webex-teams-allows-conversations-to-flow-seamlessly-between-messages-video-calls-and-realtime-whiteboarding-sessions--no-other-solution-brings-together-so-many-facets-of-collaboration-into-a-single-unified-platform-httpsdeveloper-webex-comgettingstarted-html
  version: 1.0.0
host: api.ciscospark.com
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /licenses:
    get:
      summary: List Licenses
      description: |-
        List all licenses for a given organization. If no orgId is specified, the default is the organization of the authenticated user.

        https://developer.webex.com/endpoint-licenses-get.html

        Example of a response:
        ``` json
        {
          'items' : [ {
            'id' : 'OTZhYmMyYWEtM2RjYy0xMWU1LWExNTItZmUzNDgxOWNkYzlh',
            'displayName' : 'Spark Calling',
            'totalUnits' : '42',
            'consumedUnits' : '8'
          } ]
        }
        ```
      operationId: LicensesGet
      x-api-path-slug: licenses-get
      responses:
        200:
          description: OK
      tags:
      - Video Conferencing
      - List
      - Licenses
  /licenses/{_license}:
    get:
      summary: Get License Details
      description: "Shows details for a license, by ID.\r\n\r\nSpecify the license
        ID in the licenseId parameter in the URI.\r\n\r\nhttps://developer.webex.com/endpoint-licenses-licenseId-get.html\r\n\r\nExample
        Response:\r\n``` json\r\n{\r\n  'id' : 'OTZhYmMyYWEtM2RjYy0xMWU1LWExNTItZmUzNDgxOWNkYzlh',\r\n
        \ 'displayName' : 'Spark Calling',\r\n  'totalUnits' : '42',\r\n  'consumedUnits'
        : \"8'\r\n}\r\n```"
      operationId: LicensesByLicenseGet
      x-api-path-slug: licenses-license-get
      parameters:
      - in: path
        name: _license
      responses:
        200:
          description: OK
      tags:
      - Video Conferencing
      - License
      - Details
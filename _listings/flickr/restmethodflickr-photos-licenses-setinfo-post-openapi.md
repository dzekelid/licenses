---
swagger: "2.0"
x-collection-name: Flickr
x-complete: 0
info:
  title: Flickr Photos Licenses Set Info
  description: Sets the license for a photo.
  version: 1.0.0
host: api.flickr.com
basePath: /services/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/?method=flickr.photos.licenses.getInfo:
    get:
      summary: Photos Licenses Get Info
      description: Fetches a list of available photo licenses for Flickr.
      operationId: getRestMethodFlickr.photos.licenses.getinfo
      x-api-path-slug: restmethodflickr-photos-licenses-getinfo-get
      parameters:
      - in: query
        name: api_key
        description: Your API application key
      - in: query
        name: format
        description: Response format
      responses:
        200:
          description: OK
      tags:
      - Photos
      - Licenses
      - GetInfo
  /rest/?method=flickr.photos.licenses.setInfo:
    post:
      summary: Photos Licenses Set Info
      description: Sets the license for a photo.
      operationId: postRestMethodFlickr.photos.licenses.setinfo
      x-api-path-slug: restmethodflickr-photos-licenses-setinfo-post
      parameters:
      - in: query
        name: api_key
        description: Your API application key
      - in: query
        name: license_id
        description: The license to apply, or 0 (zero) to remove the current license
      - in: query
        name: photo_id
        description: The id of the photo you want to update the license for
      responses:
        200:
          description: OK
      tags:
      - Photos
      - Licenses
      - SetInfo
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
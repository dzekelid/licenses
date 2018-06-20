---
swagger: "2.0"
x-collection-name: Flickr
x-complete: 1
info:
  title: Flickr
  description: explore-upload-and-organize-photos-on-flickr
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
---
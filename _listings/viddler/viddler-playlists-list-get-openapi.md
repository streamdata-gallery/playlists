---
swagger: "2.0"
x-collection-name: Viddler
x-complete: 0
info:
  title: Viddler  API Playlists List
  description: List all playlists for an account.
  termsOfService: http://www.viddler.com/terms-of-use/
  version: v2
host: api.viddler.com
basePath: /api/v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  viddler.playlists.create:
    post:
      summary: Playlists Create
      description: Create a playlist. Regular playlist represents user defined videos.
        Smart playlist updates in realtime returning videos matching selected filtering
        rules.
      operationId: playlists-create
      x-api-path-slug: viddler-playlists-create-post
      parameters:
      - in: query
        name: max_age
      - in: query
        name: max_update_date
      - in: query
        name: max_views
      - in: query
        name: min_update_date
      - in: query
        name: min_views
      - in: query
        name: name
      - in: query
        name: playlist_visibility
      - in: query
        name: Regular Playlist Params (all optional)nnvideo_ids
      - in: query
        name: sessionid
      - in: query
        name: Smart Playlist Params (all optional)nnusers
      - in: query
        name: sort
      - in: query
        name: tags
      - in: query
        name: type
      - in: query
        name: visibility
      responses:
        200:
          description: OK
      tags:
      - Viddler
      - Playlists
      - Create
  viddler.playlists.delete:
    post:
      summary: Playlists Delete
      description: 'Delete a playlist.u00a0Caution: This operation cannot be undone.'
      operationId: playlists-delete
      x-api-path-slug: viddler-playlists-delete-post
      parameters:
      - in: query
        name: playlist_id
      - in: query
        name: sessionid
      responses:
        200:
          description: OK
      tags:
      - Viddler
      - Playlists
      - Delete
  viddler.playlists.list:
    get:
      summary: Playlists List
      description: List all playlists for an account.
      operationId: playlists-list
      x-api-path-slug: viddler-playlists-list-get
      parameters:
      - in: query
        name: page
      - in: query
        name: per_page
      - in: query
        name: sessionid
      responses:
        200:
          description: OK
      tags:
      - Viddler
      - Playlists
      - List
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
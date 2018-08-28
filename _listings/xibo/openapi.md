swagger: "2.0"
x-collection-name: Xibo
x-complete: 1
info:
  title: Xibo API
  description: xibo-cms-api
  termsOfService: http://xibo.org.uk/legal
  version: 1.0.0
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /playlist/widget/googleTraffic/{playlistId}:
    post:
      summary: Add a Google Traffic Widget
      description: Add a new Google traffic Widget to the specified playlist
      operationId: WidgetGoogleTrafficAdd
      x-api-path-slug: playlistwidgetgoogletrafficplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: latitude
        description: The latitude for this weather widget, only pass if useDisplayLocation
          set to 0
      - in: formData
        name: longitude
        description: The longitude for this weather widget, only pass if useDisplayLocation
          set to 0
      - in: formData
        name: name
        description: Optional Widget Name
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget
      - in: formData
        name: useDisplayLocation
        description: Flag (0, 1) Use the location configured on display
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      - in: formData
        name: zoom
        description: How far should the map be zoomed in? The higher the number the
          closer the zoom, 1 represents entire globe
      responses:
        200:
          description: OK
      tags:
      - Google
      - Traffic
      - Widget
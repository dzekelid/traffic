---
swagger: "2.0"
info:
  title: Reddit Get Subreddit About Traffic
  description: Get the traffic for the current subreddit
  version: 1.0.0
host: www.reddit.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /r/subreddit/about/traffic:
    get:
      summary: Get Subreddit About Traffic
      description: Get the traffic for the current subreddit
      operationId: get&nbsp;RSubredditAboutTraffic
      responses:
        200:
          description: OK
      tags:
      - subreddit
      - about
      - traffic
definitions: []
x-collection-name: Reddit
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
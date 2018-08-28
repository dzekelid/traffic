swagger: "2.0"
x-collection-name: Reddit
x-complete: 1
info:
  title: Reddit
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
    get&nbsp;:
      summary: Get Subreddit About Traffic
      description: Get the traffic for the current subreddit
      operationId: get&nbsp;RSubredditAboutTraffic
      x-api-path-slug: rsubredditabouttraffic-getnbsp
      responses:
        200:
          description: OK
      tags:
      - Subreddit
      - About
      - Traffic
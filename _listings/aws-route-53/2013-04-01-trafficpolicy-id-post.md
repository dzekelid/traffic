---
swagger: "2.0"
info:
  title: AWS Route 53 API Create Traffic Policy Version
  version: 1.0.0
  description: Creates a new version of an existing traffic policy. When you create
    a new version of atraffic policy, you specify the ID of the traffic policy that
    you want to update and aJSON-formatted document that describes the new version.
    You use traffic policies to createmultiple DNS resource record sets for one domain
    name (such as example.com) or one subdomainname (such as www.example.com). You
    can create a maximum of 1000 versions of a traffic policy.If you reach the limit
    and need to create another version, you'll need to start a new trafficpolicy.Send
    a POST request to the /2013-04-01/trafficpolicy/ resource. The request body includes
    a document witha CreateTrafficPolicyVersionRequest element. The response returns
    theCreateTrafficPolicyVersionResponse element, which contains information aboutthe
    new version of the traffic policy.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /2013-04-01/trafficpolicy/Id:
    post:
      summary: Create Traffic Policy Version
      description: Creates a new version of an existing traffic policy
      operationId: createtrafficpolicyversion
      parameters:
      - in: body
        name: Comment
        description: "The comment that you specified in the CreateTrafficPolicyVersion
          request,\t\t\tif any"
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: CreateTrafficPolicyVersionRequest
        description: Root level tag for the CreateTrafficPolicyVersionRequest parameters
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: Document
        description: The definition of this version of the traffic policy, in JSON
          format
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: Id
        description: The ID of the traffic policy for which you want to create a new
          version
        type: string
      responses:
        200:
          description: OK
      tags:
      - traffic policies
definitions: []
x-collection-name: AWS Route 53
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
---
swagger: "2.0"
info:
  title: AWS Route 53 API List Traffic Policies
  version: 1.0.0
  description: 'Gets information about the latest version for every traffic policy
    that is associatedwith the current AWS account. Send a GET request to the /Amazon
    Route 53API version/trafficpolicy resource.Amazon Route 53 returns a maximum of
    100 items in each response. If you have a lot of trafficpolicies, you can use
    the maxitems parameter to list them in groups of up to100.The response includes
    three values that help you navigate from one group ofmaxitems traffic policies
    to the next:             IsTruncated           If the value of IsTruncated in
    the response is true,there are more traffic policies associated with the current
    AWS account.If IsTruncated is false, this response includes the lasttraffic policy
    that is associated with the current account.             TrafficPolicyIdMarker           If
    IsTruncated is true,TrafficPolicyIdMarker is the ID of the first traffic policy
    in the nextgroup of MaxItems traffic policies. If you want to list more trafficpolicies,
    make another call to ListTrafficPolicies, and specify the value ofthe TrafficPolicyIdMarker
    element from the response in theTrafficPolicyIdMarker request parameter.If IsTruncated
    is false, theTrafficPolicyIdMarker element is omitted from the response.             MaxItems           The
    value that you specified for the MaxItems parameter in the requestthat produced
    the current response.'
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /2013-04-01/trafficpolicies&amp;maxitems=MaxItems?trafficpolicyid=TrafficPolicyIdMarker:
    get:
      summary: List Traffic Policies
      description: Gets information about the latest version for every traffic policy
        that is associatedwith the current AWS account
      operationId: listtrafficpolicies
      parameters:
      - in: path
        name: maxitems
        description: "(Optional) The maximum number of traffic policies to be included
          in the response body\t\t\tfor this request"
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
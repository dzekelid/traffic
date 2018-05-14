---
swagger: "2.0"
info:
  title: AWS Route 53 API List Traffic Policy Versions
  version: 1.0.0
  description: 'Gets information about all of the versions for a specified traffic
    policy.Send a GET request to the /Amazon Route 53 APIversion/trafficpolicy resource
    and specify the ID of the traffic policyfor which you want to list versions.Amazon
    Route 53 returns a maximum of 100 items in each response. If you have a lot of
    trafficpolicies, you can use the maxitems parameter to list them in groups of
    up to100.The response includes three values that help you navigate from one group
    ofmaxitems traffic policies to the next:             IsTruncated           If
    the value of IsTruncated in the response is true,there are more traffic policy
    versions associated with the specified trafficpolicy.If IsTruncated is false,
    this response includes the lasttraffic policy version that is associated with
    the specified traffic policy.             TrafficPolicyVersionMarker           The
    ID of the next traffic policy version that is associated with the current AWSaccount.
    If you want to list more traffic policies, make another call toListTrafficPolicyVersions,
    and specify the value of theTrafficPolicyVersionMarker element in theTrafficPolicyVersionMarker
    request parameter.If IsTruncated is false, Amazon Route 53 omits theTrafficPolicyVersionMarker
    element from the response.             MaxItems           The value that you specified
    for the MaxItems parameter in the requestthat produced the current response.'
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /2013-04-01/trafficpolicies/Id/versions&amp;maxitems=MaxItems?trafficpolicyversion=TrafficPolicyVersionMarker:
    get:
      summary: List Traffic Policy Versions
      description: Gets information about all of the versions for a specified traffic
        policy
      operationId: listtrafficpolicyversions
      parameters:
      - in: path
        name: Id
        description: "Specify the value of Id of the traffic policy for which you
          want to list\t\t\tall versions"
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
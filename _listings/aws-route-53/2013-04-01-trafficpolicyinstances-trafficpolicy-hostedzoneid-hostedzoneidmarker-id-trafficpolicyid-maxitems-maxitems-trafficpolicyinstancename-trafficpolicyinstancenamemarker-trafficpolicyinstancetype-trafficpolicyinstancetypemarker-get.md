---
swagger: "2.0"
info:
  title: AWS Route 53 API List Traffic Policy Instances By Policy
  version: 1.0.0
  description: 'Gets information about the traffic policy instances that you created
    by using a specifytraffic policy version.NoteAfter you submit a CreateTrafficPolicyInstance
    or anUpdateTrafficPolicyInstance request, there''s a brief delay while Amazon
    Route 53creates the resource record sets that are specified in the traffic policy
    definition. Formore information, see the State response element.Send a GET request
    to the /Route 53 APIversion/trafficpolicyinstance resource and include the ID
    and version ofthe traffic policy.Amazon Route 53 returns a maximum of 100 items
    in each response. If you have a lot of trafficpolicy instances, you can use the
    MaxItems parameter to list them in groups of upto 100.The response includes five
    values that help you navigate from one group ofMaxItems traffic policy instances
    to the next:             IsTruncated               If the value of IsTruncated
    in the response is true,there are more traffic policy instances associated with
    the specified trafficpolicy.If IsTruncated is false, this response includes the
    lasttraffic policy instance that is associated with the specified traffic policy.             MaxItems               The
    value that you specified for the MaxItems parameter in the requestthat produced
    the current response.                  HostedZoneIdMarker, TrafficPolicyInstanceNameMarker,
    and TrafficPolicyInstanceTypeMarker               If IsTruncated is true, these
    values in the responserepresent the first traffic policy instance in the next
    group of MaxItemstraffic policy instances. To list more traffic policy instances,
    make another call toListTrafficPolicyInstancesByPolicy, and specify these values
    in thecorresponding request parameters.If IsTruncated is false, all three elements
    are omittedfrom the response.'
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /2013-04-01/trafficpolicyinstances/trafficpolicy&amp;hostedzoneid=HostedZoneIdMarker?id=TrafficPolicyId&amp;maxitems=MaxItems&amp;trafficpolicyinstancename=TrafficPolicyInstanceNameMarker&amp;trafficpolicyinstancetype=TrafficPolicyInstanceTypeMarker&
  : get:
      summary: List Traffic Policy Instances By Policy
      description: Gets information about the traffic policy instances that you created
        by using a specifytraffic policy version
      operationId: listtrafficpolicyinstancesbypolicy
      parameters:
      - in: query
        name: CapacityId
        description: The ID that identifies the provisioned capacity unit
        type: string
      - in: query
        name: ExpirationDate
        description: The date that the provisioned capacity unit expires, in Coordinated                            Universal
          Time (UTC)
        type: string
      - in: path
        name: hostedzoneid
        description: "For the first request to ListTrafficPolicyInstancesByPolicy,
          omit this\t\t\tvalue"
        type: string
      - in: query
        name: StartDate
        description: The date that the provisioned capacity unit was purchased, in
          Coordinated                            Universal Time (UTC)
        type: string
      - in: query
        name: TagKeys
        description: A list of tag keys
        type: string
      - in: query
        name: Tags
        description: The tags attached to the vault
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
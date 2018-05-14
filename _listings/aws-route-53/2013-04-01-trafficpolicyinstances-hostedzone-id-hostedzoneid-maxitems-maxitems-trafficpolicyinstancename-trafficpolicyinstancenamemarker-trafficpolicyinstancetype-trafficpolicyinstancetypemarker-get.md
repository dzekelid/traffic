---
swagger: "2.0"
info:
  title: AWS Route 53 API List Traffic Policy Instances By Hosted Zone
  version: 1.0.0
  description: 'Gets information about the traffic policy instances that you created
    in a specifiedhosted zone.NoteAfter you submit an UpdateTrafficPolicyInstance
    request, there''s a briefdelay while Amazon Route 53 creates the resource record
    sets that are specified in the traffic policydefinition. For more information,
    see the State response element.Send a GET request to the /Amazon Route 53 APIversion/trafficpolicyinstance
    resource and include the ID of the hostedzone.Amazon Route 53 returns a maximum
    of 100 items in each response. If you have a lot of trafficpolicy instances, you
    can use the MaxItems parameter to list them in groups of upto 100.The response
    includes four values that help you navigate from one group ofMaxItems traffic
    policy instances to the next:             IsTruncated               If the value
    of IsTruncated in the response is true, there aremore traffic policy instances
    associated with the current AWS account.If IsTruncated is false, this response
    includes the lasttraffic policy instance that is associated with the current account.             MaxItems           The
    value that you specified for the MaxItems parameter in the requestthat produced
    the current response.                  TrafficPolicyInstanceNameMarker and TrafficPolicyInstanceTypeMarker               If
    IsTruncated is true, these two values in the responserepresent the first traffic
    policy instance in the next group of MaxItemstraffic policy instances. To list
    more traffic policy instances, make another call toListTrafficPolicyInstancesByHostedZone,
    and specify these values in thecorresponding request parameters.If IsTruncated
    is false, all three elements are omittedfrom the response.'
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /2013-04-01/trafficpolicyinstances/hostedzone?id=HostedZoneId&amp;maxitems=MaxItems&amp;trafficpolicyinstancename=TrafficPolicyInstanceNameMarker&amp;trafficpolicyinstancetype=TrafficPolicyInstanceTypeMarker
  : get:
      summary: List Traffic Policy Instances By Hosted Zone
      description: Gets information about the traffic policy instances that you created
        in a specifiedhosted zone
      operationId: listtrafficpolicyinstancesbyhostedzone
      parameters:
      - in: path
        name: id
        description: "The ID of the hosted zone for which you want to list traffic
          policy\t\t\tinstances"
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
---
name: AWS Route 53
description: Amazon Route 53 is a highly available and scalable cloud Domain Name
  System (DNS) web service. It is designed to give developers and businesses an extremely
  reliable and cost effective way to route end users to Internet applications by translating
  names like www.example.com into the numeric IP addresses like 192.0.2.1 that computers
  use to connect to each other. Amazon Route 53 is fully compliant with IPv6 as well.nAmazon
  Route 53 effectively connects user requests to infrastructure running in AWS ndash;
  such as Amazon EC2 instances, Elastic Load Balancing load balancers, or Amazon S3
  buckets ndash; and can also be used to route users to infrastructure outside of
  AWS. You can use Amazon Route 53 to configure DNS health checks to route traffic
  to healthy endpoints or to independently monitor the health of your application
  and its endpoints. Amazon Route 53 Traffic Flow makes it easy for you to manage
  traffic globally through a variety of routing types, including Latency Based Routing,
  Geo DNS, and Weighted Round Robinmdash;all of which can be combined with DNS Failover
  in order to enable a variety of low-latency, fault-tolerant architectures. Using
  Amazon Route 53 Traffic Flowrsquo;s simple visual editor, you can easily manage
  how your end-users are routed to your applicationrsquo;s endpointsmdash;whether
  in a single AWS region or distributed around the globe. Amazon Route 53 also offers
  Domain Name Registration ndash; you can purchase and manage domain names such as
  example.com and Amazon Route 53 will automatically configure DNS settings for your
  domains.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
x-kinRank: "8"
x-alexaRank: ""
tags:
- DNS
- Amazon Web Services
created: "2018-03-24"
modified: "2018-03-24"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic/master/_listings/aws-route-53/apis.yaml
specificationVersion: "0.14"
apis:
- name: AWS Route 53 API
  description: Amazon Route 53 is a highly available and scalable cloud Domain Name
    System (DNS) web service
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: ""
  baseURL: :///
  tags: Traffic
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic/master/_listings/aws-route-53/2013-04-01-trafficpolicyinstances-trafficpolicy-amp;hostedzoneid-hostedzoneidmarker-id-trafficpolicyid-amp;maxitems-maxitems-amp;trafficpolicyinstancename-trafficpolicyinstancenamemarker-amp;trafficpolicyinstancetype-trafficpolicyinstancetypemarker-get.md
- name: AWS Route 53 API Update Traffic Policy Instance
  description: Updates the resource record sets in a specified hosted zone that were
    created based onthe settings in a specified traffic policy version.Send a POST
    request to the /2013-04-01/trafficpolicyinstance/traffic policy ID            resource.
    The request body must include a document with anUpdateTrafficPolicyInstanceRequest
    element.When you update a traffic policy instance, Amazon Route 53 continues to
    respond to DNS queriesfor the root resource record set name (such as example.com)
    while it replaces one group ofresource record sets with another. Amazon Route
    53 performs the following operations:Amazon Route 53 creates a new group of resource
    record sets based on the specified trafficpolicy. This is true regardless of how
    substantial the differences are between theexisting resource record sets and the
    new resource record sets. When all of the new resource record sets have been created,
    Amazon Route 53 starts to respondto DNS queries for the root resource record set
    name (such as example.com) by using thenew resource record sets.Amazon Route 53
    deletes the old group of resource record sets that are associated with theroot
    resource record set name.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: http:://{host}//
  tags: Traffic
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/traffic/master/_listings/aws-route-53/2013-04-01-trafficpolicyinstance-id-post.md
x-common:
- type: x-documentation
  url: http://docs.aws.amazon.com/Route53/latest/APIReference/
- type: x-faq
  url: https://aws.amazon.com/route53/faqs/
- type: x-forum
  url: https://forums.aws.amazon.com/forum.jspa?forumID=87
- type: x-pricing
  url: https://aws.amazon.com/route53/pricing/
- type: x-registrar-policies
  url: https://aws.amazon.com/route53/amazon-registrar-policies/
- type: x-service-health
  url: http://status.aws.amazon.com/
- type: x-service-level-agreement
  url: https://aws.amazon.com/route53/sla
- type: x-sla
  url: https://aws.amazon.com/route53/sla/
- type: x-website
  url: https://aws.amazon.com/route53/
- type: x-documentation
  url: http://docs.aws.amazon.com/Route53/latest/APIReference/
- type: x-faq
  url: https://aws.amazon.com/route53/faqs/
- type: x-forum
  url: https://forums.aws.amazon.com/forum.jspa?forumID=87
- type: x-pricing
  url: https://aws.amazon.com/route53/pricing/
- type: x-registrar-policies
  url: https://aws.amazon.com/route53/amazon-registrar-policies/
- type: x-service-health
  url: http://status.aws.amazon.com/
- type: x-service-level-agreement
  url: https://aws.amazon.com/route53/sla
- type: x-sla
  url: https://aws.amazon.com/route53/sla/
- type: x-website
  url: https://aws.amazon.com/route53/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---
## Simple

If multiple values are returned, random one is chosen by the client

## Weighted

Control the percentage of the requests that go to each specific resource

## Latency-based

Redirect to the resource that has the least latency (based on traffic between the users and AWS Regions)

## Failover (Active-Passive)

Healthcheck mandatory, if fail try the failover one

## Geolocation

Based on user location

## Geoproximity

Shift traffic within region by bias

## IP-based

Based on list of CIDRs for clients

## Multi Value


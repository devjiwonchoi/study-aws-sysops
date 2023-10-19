## On-Demand

- short workload
- predictable pricing
- pay by second
- Linux / Windows - billing per second
- Others - billing per hour

## Reserved (1 || 3 yrs)

- long workloads
- reserve the instance type, region, **tenancy**, os
- upfront payment
	- discount: none < partial < all 
- buy and sell the instances (wow)
#### Convertible Reserved Instances

- change instance type, instance family, OS, scope and tenancy

## Saving Plans (1 || 3 yrs)

- long workloads
- discount based on long-term usage
- beyond the plan is payed as [[#On-Demand]]

## Spot Instances

- Cheapest, but risky
- Set max price, and if exceeded, will be terminated
- Good for batch jobs, data analysis, image processing, ANY Distributed Workloads

Details on [[Spot Instance Request]]

## Dedicated Hosts

- rent a physical server
- best suite if requires the server-bound licenses (e.g. BYOL Bring Your Own License)
- more access to hardware than [[#Dedicated Instances]]
- purchasing options
	- On-Demand
	- Reserved 

## Dedicated Instances

- also rent a physical server
- may share hardware with other instances in same account

## Capacity Reservation

- Reserve the On Demand instances, to ensure it'll be ready when needed.
- Charged even when not running an instance
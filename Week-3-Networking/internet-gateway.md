# Internet Gateway

## What Is an Internet Gateway?
An Internet Gateway (IGW) is a horizontally scaled, redundant AWS component that connects a VPC to the internet.

## Why It Is Required
- Without an IGW, resources in public subnets cannot communicate with the internet.  
- Applications would be isolated, preventing user access and blocking outbound traffic (e.g., software updates).

## How Traffic Flows
1. User request originates from the internet.  
2. Traffic passes through the Internet Gateway.  
3. Routed into the public subnet.  
4. Delivered to the EC2 instance or load balancer.  

## What Happens Without an IGW
- EC2 instances cannot download patches or updates.  
- Users cannot reach web applications.  
- The VPC remains isolated, useful only for private workloads.


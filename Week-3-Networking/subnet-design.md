# Public vs Private Subnets

## Public Subnet
A public subnet is a network segment within a VPC that has a route to the Internet Gateway.  
- **Internet access**: Resources can send/receive traffic directly from the internet.  
- **Typical resources**: Web servers, load balancers, bastion hosts.  
- **Use case**: Hosting applications that must be publicly reachable.

## Private Subnet
A private subnet is a network segment without direct internet access.  
- **Internet access**: No direct route to the Internet Gateway.  
- **Typical resources**: Databases, internal services, backend applications.  
- **Use case**: Protecting sensitive workloads from exposure.

## Comparison Table

| Feature            | Public Subnet                  | Private Subnet                  |
|--------------------|--------------------------------|---------------------------------|
| Internet access    | Yes, via Internet Gateway      | No direct access                |
| Typical resources  | Web apps, Load balancers       | Databases, Internal systems     |
| Exposure           | Higher, external traffic flows | More secure, internal only      |
| Security posture   | Must be hardened               | Naturally protected             |

## Security Insight
Best practice: keep sensitive systems (databases, internal APIs) in private subnets and expose only necessary endpoints in public subnets.


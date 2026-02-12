
# ELB (Elastic Load Balancer)
```
- Load Balancer automatically distributes the incoming web traffic to available servers
- Distributes load to available server automatically
- If Load Balancer gets crashed then it does not affect any server or user
- It is region specific
- While using this you are charged hourly
- Deleting ELB does not affect or delete EC2 instance registered within it
- Registered instance are those instances that are defined under the ELB
  also known as target group
- An ELB listeners is the process that checks for connection request
- Frontend Listeners check for traffic from client to the ELB
- Backend Listeners checks the traffic from the ELB to the available instance or
  healthy instance
- A health check is a test to confirm the availability of backend server
- Target group: Logical grouping of targets behind the ELB, target group can contain
  upto 200 target
```
![image alt](https://github.com/Ashu-1808/AWS-cloud-computing-for-devops/blob/e51ee856ba0aef781144e97fa634ad1ef3533079/1741338423279.gif)
```
Types of Load Balancer:
1. Application Load Balancer (ALB)
 - Works at: OSI Layer 7 (HTTP/HTTPS)
 - Feature: Supports microservices and containers
  SSL/TLS termination, Native integration with ECS, EKS
 - Use when: ALB is best for smart routing at the application layer, REST APIs

2. Network Load Balancer (NLB)
 - Works at: OSI Layer 4 (TCP, UDP, TLS)
 - Feature: Handle millions of requests per second
  Low latency, Static IP support, ideal for non HTTP traffic
 - Used when: NLB is for speed, scale and low latency
  (Database/messaging), TCP/UDP
  High performance workload
  Real-Time systems

3. Classic Load Balancer (CLB) (Legacy)
 - Works at: OSI Layer 4 / Basic Layer 7
 - Feature: Older generation, limited routing capacity
 - Used for: Maintaining legacy system only
 - Note: Not for new application

4. Gateway Load Balancer (GLB)
 - Works at: OSI Layer 3/4 (Network traffic inspection)
 - Feature: Designed for security application
  Integrate with firewalls, IDS/IPS
 - Used at: GLB is for security, not web traffic
  Firewall security, Centralized network security

ELB Advantages:
 1. High Availability
 2. Health checks → No downtime
 3. Auto scaling → Traffic to healthy targets only
 4. Security → Handles traffic spikes
 5. Cost efficient → Pay as you go

ELB Disadvantages:
 1. Debugging is most difficult
 2. Vendor lock-in → Hard to migrate
 3. Limited control → less tuning
 4. Limits → Depends on ELB type



Health Checks :
They determine whether a target is healthy and able to receive traffic
1. Healthy threshold:
  No. of consecutive successful health checks required before target is marked healthy
  Eg: If healthy threshold is 3 → then target must pass 3 continuous checks

2. Unhealthy threshold:
  Number of consecutive health checks required before target is marked unhealthy
  Eg: If unhealthy threshold is 4 → After 4 target failures, traffic stops

3. Timeout:
  Maximum time ELB waits for a response from target
  Eg: If timeout is 5 seconds → No response within 5 second = failure
  (Should be less than interval time)

4. Interval:
  Time between consecutive health check request
  Eg: If interval is 30 seconds → Health check happens every 30 seconds
  (Smaller than timeout)

```

# Autoscaling Theory

## At a high level

Autoscaling in AWS has 3 major organizational units.

* Groups - group of resources such as EC2 instances
* Configuration Template - a launch configuration for EC2 instances (including AMI ID, instance type, key pair to be used, security groups and block device mapping.)
* Scaling Options - A set of configuration options which dictate how groups will scale based on the occurrence of specified conditions.

## Scaling Options

While the first two components of autoscaling are rather obvious (what to scale), scaling options are HOW/WHEN to scale.

There are currently 5 types of scaling options in AWS.

1. Maintain current instance levels at all times
    * Maintain a specified number of running instances at all times.
    * Does so by performing periodic health checks on running instances. If a running instance is determined to be unhealthy it is terminated and a new instance launched in its place.
2. Manual scaling
    * Most basic type of scaling
    * You literally manually say when you want groups to scale up and down.
    * AWS EC2 Autoscaling manages this process once you decide what you want to do
3. Scale based on a schedule
    * Scaling actions are performed automatically as a function of date and time.
    * Good when you have highly predictable demand.
4. Scale based on demand
    * Advanced form of autoscaling.
    * Uses scaling policies which define parameters which control the scaling process.
      * Scale when CPU usage across the group exceeds 50% etc.
    * Typically the best choice for applications which have highly unpredictable demand.
5. Predictive scaling
    * Use Amazon EC2 Autoscaling in combination with AWS autoscaling to scale resources across multiple services
    * AWS Autoscaling can help maintain optimal availability and performance by combining predictive scaling and dynamic (demand-based) scaling (proactive and reactive, respectively) to scale EC2 capacity faster
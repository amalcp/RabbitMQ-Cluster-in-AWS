

<!-- ![alt text](https://github.com/amalcp/RabbitMQ-Cluster-in-AWS/blob/master/imgs/RMQ.png) -->
<p align="center"> 
<img src="https://github.com/amalcp/RabbitMQ-Cluster-in-AWS/blob/master/imgs/RMQ.png">
</p>

# AWS RabbitMQ Cluster with Loadbalancer
This is AWS cloudformation template will create your entaire stack with zero down time, ie, elb with auto scaling group.
Please note the CUP metrics to scale up & down of your auto scaling group
  
#### Notes!

  - See the output section in the cloudformation stack to get 
        - ELB End Point
        - Login Details
  - Need to change default culuster admin password? 
        - Update the userdata in the launch config
- Look at `cloud-config.yml` to see the user data

#### Port Numbers 
- 4369: epmd
- 5672: AMQP
- 15672: HTTP (API & Dashboard)
- 8883: Secure-mqtt

## Spin Up the Cluster


### Using AWS Console
1. Login to AWS console & navigate to CloudFormation template 
2. Create Stack 
3. Upload the `rabbitmq-cf-template.json`
4. Copy the values from output tab
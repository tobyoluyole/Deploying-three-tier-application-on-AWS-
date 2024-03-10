DEPLOYMENT OF THREE-TIER APPLICATION ON AWS 

The Project above deploys a three-tier application on AWS. The necessary network, security, app, and database components and configurations were manually created to run this architecture in an available and scalable manner.

Architecture Overview
![3TierArch](https://github.com/tobyoluyole/Deploying-three-tier-application-on-AWS-/assets/105201994/9abe8f47-901a-41e5-9bee-734c14911d3f)
The architecture above shows a public-facing Application Load Balancer that forwards client traffic to the web tier EC2 instances. The web tier is running Nginx web servers that are configured to serve a React.js website and redirect  API calls to the application tier’s internal facing load balancer. The internal facing load balancer then forwards that traffic to the application tier written in Node.js. The application tier manipulates data in an Aurora MySQL multi-AZ database and returns it to the web tier. Load balancing, health checks and autoscaling groups are created at each layer to maintain the availability of this architecture.

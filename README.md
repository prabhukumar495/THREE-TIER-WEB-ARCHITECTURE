# THREE-TIER-WEB-ARCHITECTURE
Three tier web application with appropriate security layers

In this architecture, a public-facing Application Load Balancer forwards client traffic to our web tier EC2 instances. The web tier is running Nginx webservers that are configured to serve a React.js website and redirects our API calls to the application tier’s internal facing load balancer. The internal facing load balancer then forwards that traffic to the application tier, which is written in Node.js. The application tier manipulates data in an Aurora MySQL multi-AZ database and returns it to our web tier. Load balancing, health checks and autoscaling groups are created at each layer to maintain the availability of this architecture.
![3TierArch](https://github.com/prabhukumar495/THREE-TIER-WEB-ARCHITECTURE/assets/109064542/416a0765-aae7-44b9-9025-367e8cc87305)

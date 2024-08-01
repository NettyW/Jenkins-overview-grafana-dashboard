# Jenkins Dashboard.
![icon](https://github.com/NettyW/Jenkins-overview-grafana-dashboard/blob/main/imgs/i.jpg?raw=true)
## Description.
The dashboard displays the status of your jenkins jobs, the status of the queue on executors, and a few other things. The metrics you get are taken from the Prometheus plugin for your Jenkins.

## Installing and configuration.

1. Import the Dashbord with json [file](https://github.com/NettyW/Jenkins-overview-grafana-dashboard/blob/main/dashboard/Jenkins%20overview.json) or import with Dashboard ID - `21628`
https://grafana.com/grafana/dashboards/21628-jenkins-overview/
2. Configure your `prometheus` plugin in **Jenkins**.
![prometheus_params](https://github.com/NettyW/Jenkins-overview-grafana-dashboard/blob/main/imgs/4.png?raw=true)
For the dashboard to work, you need to configure your **prometheus plugin** for jenkins. Set the default name for metrics on prometheus like `prometheus_`. All your metrics should start with `prometheus_`.
And parameter *"Job attribute name"* must be `jenkins_job`


For interactivity, also include a link to your Jenkins in the variables. **jenkins_url** must be like `https://jenkins-test.com/job/`. 

Tested on jenkins 2.346.3 only!
# dev_ResearchMonitorRH7
Research Monitoring Development 

#### Open Source Monitoring
- Sentry started life as a Python-only monitoring project but can now be used for any programming language. [https://github.com/getsentry/sentry](https://github.com/getsentry/sentry) <br/>
- Service Canary [https://servicecanary.com/](https://servicecanary.com/) <br/>
- ping.gg [https://ping.gg/](https://ping.gg/) <br/>
- glance [https://nicolargo.github.io/glances/](https://nicolargo.github.io/glances/) <br/>s
- statsd  is a node.js network daemon that listens for metrics and aggregates them for transfer into another service such as Graphite. [https://github.com/etsy/statsd/](https://github.com/etsy/statsd/) <br/>
- Graphite stores time-series data and displays them in graphs through a Django web application. [https://graphite.readthedocs.org/en/latest/overview.html](https://graphite.readthedocs.org/en/latest/overview.html) <br/>
- Sensu is an open source monitoring framework written in Ruby but applicable to any programming language web application [http://sensuapp.org/](http://sensuapp.org/) <br/> 
- Graph Explorer by Vimeo is a Graphite-based dashboard with added features and a slick design. [http://vimeo.github.io/graph-explorer/](http://vimeo.github.io/graph-explorer/) <br/>
- Munin is a client plugin-based monitoring system that sends monitoring traffic to the Munin node where the data can be analyzed and visualized. Note this project is written in Perl so Perl 5 must be installed on the node collecting the data [http://munin-monitoring.org/](http://munin-monitoring.org/) <br/>n
- Bucky measures the performance of a web application from end user's browsers and sends that data back to the server for collection  [https://github.com/HubSpot/BuckyClient](https://github.com/HubSpot/BuckyClient) <br/>

#### Jenkins HTML Publisher
[https://plugins.jenkins.io/htmlpublisher/](https://plugins.jenkins.io/htmlpublisher/) <br/>

#### Jenkins CI/CD Pipeline
![Jenkins Pipeline](https://github.com/lel99999/dev_ResearchMonitorRH7/blob/main/JenkinsCICd-01.PNG) <br/>

Script directly or upload Jenkinsfile: <br/>

```
pipeline {
   agent any

   stages {
      stage('Build') {
        steps {
          echo 'Building...'
          echo "Running ${env.BUILD_ID} ${env.BUILD_DISPLAY_NAME} on ${env.NODE_NAME} and JOB ${env.JOB_NAME}"
        }
   }
   stage('Test') {
     steps {
        echo 'Testing...'
     }
   }
   stage('Deploy') {
     steps {
       echo 'Deploying...'
     }
   }
  }
}
```

#### ToDo
- Jenkins CI/CD Workflow for HTML Conversion
- Inline Graphics Generation

#### Notes
- 1 and 2 Level Descent


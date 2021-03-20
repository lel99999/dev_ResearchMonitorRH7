# dev_ResearchMonitorRH7
Research Monitoring Development 

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


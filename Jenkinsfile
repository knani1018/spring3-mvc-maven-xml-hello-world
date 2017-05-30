pipeline {
    agent { label "jenkinsmaster" }

    stages {
      stage('build') {
        steps {
          sh 'mvn package'
        }
      }      
      stage('deploy') {
          steps {
              sh 'chmod 655 /var/lib/jenkins/workspace/pipeline-project/target/*.war'
              sh 'cp -r /var/lib/jenkins/workspace/pipeline-project/target/*.war /opt/tomcat7/webapps/'
          }          
      }
    }
}

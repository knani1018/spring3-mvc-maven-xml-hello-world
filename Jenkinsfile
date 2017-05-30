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
              sh 'pwd'
              sh 'sudo chmod 655 /var/lib/jenkins/workspace/pipeline-test/target/*.war'
              sh 'sudo cp -r /var/lib/jenkins/workspace/pipeline-test/target/*.war /opt/tomcat7/webapps/'
          }          
      }
    }
}

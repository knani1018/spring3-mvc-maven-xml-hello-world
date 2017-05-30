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
              sh 'cd /var/lib/jenkins/workspace/pipeline-project/target/; sudo chmod 655 *.war'
              sh 'sudo cp -r /var/lib/jenkins/workspace/pipeline-project/target/*.war /opt/tomcat7/webapps/'
          }          
      }
    }
}

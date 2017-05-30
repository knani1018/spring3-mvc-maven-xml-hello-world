pipeline {
    agent { label "jenkinsmaster" }

    stages {
      stage('build') {
        steps {
          sh 'mvn package'
        }
      }      
      stage('deploy'){
          steps {
            sh 'cp /var/lib/jenkins/workspace/pipeline-project/target/*.war opt/tomcat7/webapps/'
          }          
      }
    }
}

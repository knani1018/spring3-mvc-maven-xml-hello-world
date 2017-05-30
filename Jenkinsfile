pipeline {
    agent { label "jenkinsmaster" }

    stages {
      stage('build') {
        steps {
          sh 'mvn package'
        }
      }
    }
}

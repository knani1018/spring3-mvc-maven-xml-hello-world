pipeline {
    agent jenkins-master

    stages {
      stage('build') {
        steps {
          sh 'mvn package'
        }
      }
    }
}

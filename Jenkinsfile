pipeline {
    agent any
  stages {
    stage('build') {
      steps {
        bat "mvn clean"
      }
    }
    stage('Test') {
      steps {
        bat "mvn test"
      }
    }
    stage('Deploy') {
      steps {
        bat "mvn package"
      }
    }
      stage ('list directory') {
          if (isUnix()) {
              sh "ls -la"
          } else {
              bat "dir"
          }
      }
  }
}

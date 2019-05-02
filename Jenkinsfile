pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'mvn clean package'
          }
        }
        stage('abcd') {
          steps {
            build 'abcd'
          }
        }
      }
    }
  }
}
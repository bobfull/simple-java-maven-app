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
    stage('') {
      steps {
        build(job: 'simple-java-maven-app', propagate: true, quietPeriod: 5, wait: true)
      }
    }
  }
}
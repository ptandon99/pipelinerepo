pipeline {
  agent {
    label 'jdk8'
  }
  stages {
    stage('SayHello') {
      parallel {
        stage('SayHello') {
          steps {
            echo 'Hello ${MY_NAME}!'
          }
        }
        stage('java version') {
          steps {
            sh 'java -version'
          }
        }
      }
    }
    stage('newhello') {
      steps {
        echo 'new hello'
      }
    }
  }
  environment {
    MY_NAME = 'Mary'
  }
}
pipeline {
  agent any
  stages {
    stage('SayHello') {
      parallel {
        stage('SayHello') {
          steps {
            echo 'Hello World'
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
}
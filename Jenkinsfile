pipeline {
  agent {
    label 'jdk8'
  }
  stages {
    stage('SayHello') {
      parallel {
        stage('SayHello') {
          steps {
            echo "Hello ${MY_NAME}!"
            echo "${TEST_USER_USR}"
            echo "${TEST_USER_PSW}"
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
    TEST_USER = credentials('test-user')
  }
}
pipeline {
  agent {
    label 'jdk8'
  }
  stages {
    stage('SayHello') {
      parallel {
        stage('SayHello') {
          steps {
            echo "Hello ${params.Name}"
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
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}
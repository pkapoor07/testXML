pipeline {
  agent {
    label 'jdk9'
  }
  stages {
    stage('Hello') {
      parallel {
        stage('Hello') {
          steps {
            echo 'Hello World'
            sh '''java -version
echo "Hello ${MY_NAME}!"
echo "Hello ${BUDDY_NAME}!"'''
            sleep 1
          }
        }
        stage('Dont say Hello') {
          steps {
            echo 'See Yaa'
          }
        }
      }
    }
  }
  environment {
    MY_NAME = 'Puneet'
    BUDDY_NAME = 'Anthony'
  }
}
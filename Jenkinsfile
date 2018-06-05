pipeline {
  agent any
  stages {
    stage('Hello') {
      parallel {
        stage('Hello') {
          steps {
            echo 'Hello World'
            sh 'java -version'
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
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
            # echo "Hello ${params.Name}!"
            echo "Hello ${BUDDY_NAME}!"'''
            sleep 1
          }
        }
        stage('Dont say Hello') {
          steps {
            echo 'See Yaa'
            sh '''echo "${TEST_USER_USR}"
            echo "${TEST_USER_PSW}"'''
          }
        }
      }
    }
  }
  environment {
    MY_NAME = 'Puneet'
    BUDDY_NAME = 'Anthony'
    TEST_USER = credentials('test-user')
  }
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}
pipeline {
  agent none
  stages {
    stage ('build') {
    agent any
       steps {
          sh '''
                  echo "this is build stage"
                  sleep 2
             '''
             }
    }
    stage ('deploy') { 
    parallel {
    stage ('deploy1') {
    agent { label 'slave-02' }
       steps {
          sh '''
                  echo "this is deploy stage"
                  sleep 2
             '''
             }
    }
      stage ('deploy2') {
    agent { label 'slave-02' }
       steps {
          sh '''
                  echo "this is deploy stage"
                  sleep 2
             '''
             }
    }
    }
    }
    stage ('test') {
    agent any
       steps {
          sh '''
                  echo "this is test stage"
                  sleep 2
             '''
             }
    }
  }
}

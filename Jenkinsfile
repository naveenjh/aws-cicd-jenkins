pipeline {
  agent any
 stages {
    stage('Build') {
      steps {
          echo 'Building..'
      }
    }
    stage('Test') {
      steps {
          echo 'Testing..'
      }
    }
    stage('Deploy') {
      steps {
          echo 'Deploying....'
      }
    }
    }
  environment {
    development = 'dev'
    stage = 'stage'
    prod = 'prod'
  }
}
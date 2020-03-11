pipeline {
  agent any
  stages {
    stage('Dev') {
      parallel {
        stage('Dev') {
          steps {
            echo 'Hello Naveen in Dev Pipeline'
          }
        }

        stage('Stage') {
          steps {
            echo 'Hello Naveen in Stage pipeline'
          }
        }

        stage('Prod') {
          steps {
            echo 'Hello Naveen in Prod pipeline'
          }
        }

      }
    }

  }
  environment {
    development = 'dev'
    stage = 'stage'
    prod = 'prod'
  }
}
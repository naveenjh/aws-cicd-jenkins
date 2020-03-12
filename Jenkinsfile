pipeline {
  agent any
 stages {
    stage('Build') {
      steps {
          sh 'echo "hello world"'
          sh '''
           echo "Multiline works too"
           ls -lah
           '''
      }
    }   
  }
 
}
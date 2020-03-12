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
    stage('Upload to AWS') {
        steps {
          withAWS(region:'us-east-1',credentials:aws-static) {
            s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'index.html', bucket:'njha-udacity-static')
          }
        }   
  }
 
}
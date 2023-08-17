pipeline {
    agent any
    stages{
      stage('deploy to S3'){
          steps{
              withAWS(credentials: 'aws-jenkins-demo', region: 'us-east-1') {
                   sh 'echo "hello Sinaj">hello.txt'
                   s3Upload acl: 'Private', bucket: 'jenkin-s3', file: 'hello.txt'

           
             
              }
          }
      }
  }
}

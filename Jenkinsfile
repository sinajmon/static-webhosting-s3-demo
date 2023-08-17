pipeline {
    agent any
    stages{
      stage('deploy to S3'){
          steps{
              withAWS(credentials: 'aws-jenkins-demo', region: 'us-east-1') {
                   sh 'echo "hello Sinaj">hello.txt'
                 sh 'aws s3 cp hello.txt s3://jenkins-s3'
 
           
             
              }
          }
      }
  }
}

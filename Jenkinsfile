pipeline {
    agent any
    stages{
      stage('deploy to S3'){
          steps{
              withAWS(credentials: 'aws-jenkins-demo', region: 'us-east-1') {
                    sh 'aws s3 cp Code/index.html s3://jenkins-s3'
                   sh 'aws s3 cp public/error.html s3://jenkins-s3'
           
             
              }
          }
      }
  }
}

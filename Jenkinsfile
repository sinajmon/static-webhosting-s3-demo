pipeline {
    agent any
    stages{
      stage('deploy to S3'){
          steps{
              withAWS(credentials: 'aws-jenkins-demo', region: 'us-east-1') {
              sh 'aws s3 cp Code/index.html s3://jenkins-s3-demo'
              sh 'aws s3api put-object-acl --bucket jenkins-s3-demo --key index.html --acl public-read'  
              sh 'aws s3 cp public/error.html s3://jenkins-s3-demo'
              sh 'aws s3api put-object-acl --bucket <bucket-name> --key error.html --acl public-read'
              }
          }
      }
  }
}

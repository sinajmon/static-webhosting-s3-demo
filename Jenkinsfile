pipeline {
    agent any
    stages{
      stage('deploy to S3'){
          steps{
              sh 'aws s3 cp Code/index.html s3://jenkins-s3-demo'
              sh 'aws s3api put-object-acl --bucket jenkins-s3-demo --key index.html --acl public-read'             
          }
      }
  }
}

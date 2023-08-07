pipeline {
    agent any
    stages{
      stage('deploy to S3'){
          steps{
              sh '/usr/local/bin/aws s3 cp Code/index.html s3://jenkins-s3-demo'
              sh '/usr/local/bin/aws s3api put-object-acl --bucket jenkins-s3-demo --key index.html --acl public-read'             
          }
      }
  }
}

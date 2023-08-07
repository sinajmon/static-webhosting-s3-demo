pipeline {
    agent any
    stages {
        stage('deploy') {
            steps {
              sh "aws configure set region 'us-east-1" 
              sh "aws configure set aws_access_key_id 'AKIATSMVQX4KXUYQGMWR"  
              sh "aws configure set aws_secret_access_key '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"
              sh "aws s3 cp Code/index.html s3://my-static-bucket-jenkins"
            }
        }
    }
}

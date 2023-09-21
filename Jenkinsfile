pipeline {
    agent any
    stages {
        stage('Copy to S3') {
            steps {
                withAWS(region: 'us-east-1', credentials: 'aws-jenkins-demo') {
                    sh "aws s3 cp Code/index.html s3://jenkin-s3"
                }
            }
        }
    }
}

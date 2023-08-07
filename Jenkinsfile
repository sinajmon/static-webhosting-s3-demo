pipeline {
    agent any
    stages {
        stage('deploy') {
		 steps {
                withAWS(region: 'us-east-1', credentials: 'aws-jenkins-demo') {
                   h "aws s3 cp Code/index.html s3://jenkins-s3-demo"
                }
            
        }
    }
}

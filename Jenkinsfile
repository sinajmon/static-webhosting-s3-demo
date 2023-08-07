pipeline {
    agent any
    stages {
        stage('deploy') {
		 steps {
                withAWS(region: 'us-east-1', credentials: 'aws-jenkin') {
	           s3Upload(file:'index.html', bucket:'jenkins-s3-demo', path:'Code/index.html')
                }
            
        }
    }
 }
}

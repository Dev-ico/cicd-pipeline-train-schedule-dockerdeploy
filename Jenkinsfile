pipeline {
    agent { label 'master' }
    environment {
	    DOCKERHUB_CREDENTIALS=credentials('docker_hub_login')
	}
    stages {
        stage('Push Docker Image') {
            when {
                branch 'master'
            }
            steps {
		        sh 'echo $DOCKERHUB_CREDENTIALS_PSW > /tmp/psw.txt'
                sh 'echo $DOCKERHUB_CREDENTIALS_USR > /tmp/usr.txt'
            }
        }
    }
}

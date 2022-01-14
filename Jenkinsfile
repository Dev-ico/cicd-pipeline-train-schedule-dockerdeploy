pipeline {
    agent { label 'master' }
    environment {
	    DOCKERHUB_CREDENTIALS=credentials('97f0d786-cec3-44b2-9e97-e3c1d2267f7a')
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

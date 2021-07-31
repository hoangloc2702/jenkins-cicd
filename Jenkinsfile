pipeline {
	agent none
	stages {
		stage('build') {
			agent {
				docker {
					image 'node:14-slim'
					args '-u 0:0 /tmp:/root/.cache'
				}
			}
			steps {
				git branch: 'develop', credentialsId: 'jenkins_cicd_1', url: 'https://github.com/hoangloc2702/jenkins-cicd.git'
				sh 'npm install'
				sh 'npm run build'
			}
		}
	}
}
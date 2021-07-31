pipeline {
	agent {
		docker {
			image 'node:14-slim'
		}
	}
	stages {
		stage('build') {
			steps {
				git branch: 'develop', credentialsId: 'jenkins_github_userpass', url: 'https://github.com/hoangloc2702/jenkins-cicd.git'
				sh 'npm install'
			}
		}
		stage('test') {
			steps {
				sh 'npm run test'
			}
		}
	}
}
pipeline {
	agent none
	stages {
		agent {
			docker {
					image 'node:14-slim'
				}
			}
		stage('test') {
			steps {
				git branch: "${ghprbActualCommit}", credentialsId: 'jenkins_github_userpass', url: 'https://github.com/hoangloc2702/jenkins-cicd.git'
				sh 'npm install'
				sh 'npm run test'
			}
		}
	}
}
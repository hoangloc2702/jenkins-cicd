pipeline {
	agent {
		docker {
			image 'node:14-slim'
		}
	}
	stages {
		stage('build') {
			steps {
				git branch: '$BRANCH_NAME', credentialsId: 'jenkins_github_userpass', url: 'https://github.com/hoangloc2702/jenkins-cicd.git'
				echo '$BRANCH_NAME'
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
pipeline {
	agent {
		docker {
			image 'node:14-slim'
		}
	}
	stages {
		stage('build') {
			steps {
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
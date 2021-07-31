pipeline {
	agent none
	stages {
		stage('test') {
			agent {
				docker {
					image 'node:14-slim'
				}
			}
			steps {
				sh 'npm install'
				sh 'npm run test'
			}
		}
	}
}
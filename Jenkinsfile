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
				sh 'npm install'
				sh 'npm run test'
			}
		}
	}
}
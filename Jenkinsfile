pipeline {
	agent none
	stages {
		stage('build') {
			agent {
				docker {
					image 'node:14-slim'
				}
			}
			steps {
				sh 'npm install'
			}
		}
		stage('test') {
			agent {
				node {
					label 'master'
				}
			}
			steps {
				sh 'npm run test'
			}
		}
	}
}
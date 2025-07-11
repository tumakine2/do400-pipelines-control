pipeline {
	agent {
		node {
			label 'nodejs'
		}
	}
	stages {
		stage('Run tests') {
			parallel {
				stage('Backend Tests') {
					steps {			
						sh 'node ./backend/test.js'
					}	
				}
				stage('Frontend Tests') {
					steps {			
						sh 'node ./frontend/test.js'	
					}
				}
			}
		}
	}
}

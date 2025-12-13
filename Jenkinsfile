pipeline {
	agent {
		label 'ISTHARA-AGENT'
	}
	environment {
		appVersion = ''
		REGION	=	'us-east-1a'
		ACC_ID	= '291293118913'
		PROJECT	= 'isthara-roboshop'
		COMPONENT = 'catalogue'
	}
	options{
		timeout(time:30, unit: 'MINUTES')
		disableConcurrentBuilds()
		

	}
	stages {
		stage('GIT CLONE') {
			steps{
				echo 'cloning the repo from scm'
			}
		}
		stage('NPM BUILD') {
			steps{
				echo 'building the npm package'
			}
		}
		stage('TEST'){
			steps {
				echo 'TEST BUILD'
			}
		}
		stage('Deploy') {
			steps{
				echo 'deploy application on lower environment'
			}
		}
	}
	post {
		always {
			echo 'Build Runned'
			deleteDir()
		}
		failure {
			echo 'Build failed'
		}
		success {
			echo 'Build Success'
		}
	}
}
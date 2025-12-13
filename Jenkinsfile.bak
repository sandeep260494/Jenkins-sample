pipeline {
	agent any
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
}
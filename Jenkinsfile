pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				sh 'echo "Hi Toby"'
				sh '''
				    echo "Multiline works too"
				    ls -altr
                                '''
			}
		}
		stage('Test') {
			steps {
#				sh 'echo "Fail!"; exit 1'
				sh 'echo "Yes!"; exit 0'
			}
		}
	}
	post {
		always {
			echo 'This will always run'
		}
		success {
			echo 'This will only run if successful'
		}
		failure {
			echo 'This will only run if a failure happens'
		}
		unstable {
			echo 'This will only run if the test was marked unstable'
		}
		changed {
			echo 'This will only run if the state of the Pipeline has changed'
			echo 'For example if it was failed and now it is success'
		}
	}
}
				

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
	}
}
				

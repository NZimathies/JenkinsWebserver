pipeline {
	agent {
		node {
			label 'nginx'
			}
	}
	triggers {
		pollSCM '*/2 * * * *'
	}
	stages {
		stage('Changes') {
			steps {
				echo "Transferring changes to webserver..."
				sh '''
				sudo cp -f index.html /data/www/
				'''
			}
		}
	}
}

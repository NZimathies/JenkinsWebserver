pipeline {
	agent {
		node {
			label 'WebserverGit'
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
				cp -f index.html /data/www/
				'''
			}
		}
	}
}

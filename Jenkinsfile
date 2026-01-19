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
				echo "Transerring changes to webserver..."
				cp index.html /data/www/
			}
		}
	}
}

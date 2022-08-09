pipeline {

    agent any

    stages {

        stage ('Initialization') {
            steps {
                sh 'echo "Starting the build.."'
            }
        }

	stage ('Build') {
            steps {
                sh 'npm install'
	    }
        }

	stage ('NPM Audit Analysis') {
            steps {
                sh '/home/b310v3_jenkins_test/npm-audit.sh'
            }
        }

	stage ('Lint Analysis with Jshint') {
	    steps {
		sh '/home/b310v3_jenkins_test}/eslint-script.sh'
	    }
	}
    }

}

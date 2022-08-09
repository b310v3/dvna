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
                sh '''
                    export MYSQL_USER=root
                    export MYSQL_DATABASE=dvna
                    export MYSQL_PASSWORD=powerrrr
                    export MYSQL_HOST=127.0.0.1
                    export MYSQL_PORT=3306
                    npm install
                   '''
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

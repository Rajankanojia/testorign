pipeline {

    agent any
	parameters {
		choice(name: 'VERSION', choices: ]'1.1.0', '1.2.0', 1.3.0', description: 'Hello iam version')
		booleanParam(name: 'executeTests', defaultValue: true, description: 'Hello i am Boolean')
    stages {
        stage("init") {
            steps {
                echo 'initilizing application...'
            }
        }
		
        stage("build") {
            steps {
                echo 'building application...'
            }
        }
		
        stage("test") {
            when {
		expression {
		params.executeTests
				}
	}
            steps {
                echo 'testing application...'
            }
        }
        stage("deploy") {
            steps {
                echo 'deploying application...'
		echo "deploying version ${params.VERSION}"
            }
        }
    }   
}

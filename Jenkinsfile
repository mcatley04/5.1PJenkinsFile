pipeline {
    agent any

    environment {
        DIRECTORY_PATH = 'path/to/your/code'
        TESTING_ENVIRONMENT = 'staging'
        PRODUCTION_ENVIRONMENT = 'Michael'
    }

    stages {
        stage('Build') {
            steps {
                echo "Fetch the source code from the directory path: ${env.DIRECTORY_PATH}"
                echo "Compile the code and generate any necessary artifacts."
            }
        }
        stage('Test') {
            steps {
                echo "Unit tests"
                echo "Integration tests."
            }
        }
        stage('Code Quality Check') {
            steps {
                echo "Check the quality of the code."
            }
        }
        stage('Deploy') {
            steps {
                echo "deploy the application to a testing environment specified by the environment variable: ${env.TESTING_ENVIRONMENT}"
            }
        }
        stage('Approval') {
            steps {
                echo "Awaiting approval..."
                sleep 10
                echo "Approved for production."
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploy the application to a production environment specified by the environment variable ${env.PRODUCTION_ENVIRONMENT}"
            }
        }
    }
}
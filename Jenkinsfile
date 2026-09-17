pipeline {
    agent any
    parameters {
        booleanParam(name: 'RUN_TESTS', defaultValue: true, description: 'Check to run the testing phase')
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/abijithpa2024-netizen/jenkins-conditional-lab'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the application...'
            }
        }
        stage('Test Execution') {
            when {
                expression { return params.RUN_TESTS }
            }
            steps {
                echo 'Executing test suites...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
}

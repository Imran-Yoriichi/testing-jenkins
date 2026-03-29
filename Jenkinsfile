pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building the application...'
                echo "Running on branch: ${env.GIT_BRANCH}"
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                echo 'All tests passed!'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                echo "Commit being deployed: ${env.GIT_COMMIT}"
            }
        }

    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed! Check the logs.'
        }
        always {
            echo 'This runs no matter what.'
        }
    }
}

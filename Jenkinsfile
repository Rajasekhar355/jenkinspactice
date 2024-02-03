pipeline {
    agent {
        node {
            label 'Agent_Test'
        }
    }

    environment {
        GREETING='Hello'
    }

    stages {
        stage('Build') {
            steps {
                echo "buils"
            }
        }
        stage('Test') {
            steps {
                echo "Test$GREETING"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploy"
            }
        }
    }

    post {
        always {
            echo "when pipeline alwys"
        }

        success {
            echo "only success"
        }

        failure {
            echo "only failure"
        }
    }
}
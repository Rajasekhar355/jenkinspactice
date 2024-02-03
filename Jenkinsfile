pipeline {
    agent {
        node {
            label 'Agent_Test'
        }
    }
    stages {
        stage('Build') {
            steps {
                echo "buils"
            }
        }
        stage('Test') {
            steps {
                echo "Test"
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
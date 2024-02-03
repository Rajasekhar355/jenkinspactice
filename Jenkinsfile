pipeline {
    agent {
        node {
            label 'Agent_Test'
        }
    }

    environment {
        GREETING='Hello'
    }

    options {
        timeout(time: 1, unit: 'HOURS')
        disableConcurrentBuilds()
    }

    stages {
        stage('Build') {
            steps {
                echo "buils"
                sleep(100)
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
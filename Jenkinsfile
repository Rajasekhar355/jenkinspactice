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
        timeout(time: 5, unit: 'SECONDS')
        disableConcurrentBuilds()
    }

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    
    stages {
        stage('Build') {
            steps {
                echo "buils"
                sleep(10)
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
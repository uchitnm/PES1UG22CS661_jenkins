pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/uchitnm/PES1UG22CS661_jenkins.git'
            }
        }
        stage('Build') {
            steps {
                sh 'g++ hello_task5.cpp -o hello_exec '
            }
        }
        stage('Test') {
            steps {
                sh './hello_exec'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
        success{
            echo "Pipeline Successfully executed"
}
    }
}

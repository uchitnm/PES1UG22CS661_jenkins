pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/uchitnm/PES1UG22CS661_jenkins.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'sudo apt-get update && sudo apt-get install -y g++'
            }
        }
        stage('Build') {
            steps {
                sh 'set -e; g++ -o hello_exec hello_task5.cpp'
            }
        }
        stage('Test') {
            steps {
                sh 'chmod +x hello_exec'
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
        success {
            echo "Pipeline Successfully executed"
        }
    }
}

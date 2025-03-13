pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/uchitnm/PES1UG22CS661_jenkins.git'
            }
        }
        stage('Build application') {
            steps {
                sh 'g++  -o task5_1 main.cpp'  
            }
        }
        stage('Test application') {
            steps {
                sh './task5_1'  
            }
        }
        stage('Deploy application') {
            steps {
                echo 'Deploying application...'  
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed!' 
        }
        success {
            echo 'Pipeline executed successfully!'  
        }
    }
}

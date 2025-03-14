pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/rbhunia/spring-project.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Deploy to Nexus') {
            steps {
                sh 'mvn deploy'
            }
        }
    }
}
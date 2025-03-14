pipeline {
    agent {
        docker {
            image 'maven:3.8.3-openjdk-17' // Use a Maven image with JDK 17
        }
    }
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
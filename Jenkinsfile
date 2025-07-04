pipeline {
    agent any
    tools {
        maven 'Maven 3.9.4'
        jdk 'Temurin-17'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package -DskipTests'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}

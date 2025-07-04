pipeline {
    agent any
    stages {
        stage('Build with Maven') {
            steps {
                script {
                    docker.image('maven:3.9.4-eclipse-temurin-17').inside {
                        sh 'mvn clean package -DskipTests'
                    }
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    docker.image('maven:3.9.4-eclipse-temurin-17').inside {
                        sh 'mvn test'
                    }
                }
            }
        }
    }
}

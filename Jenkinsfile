pipeline {
    agent any

    environment {
        APP_PORT = '9090'
    }

    tools {
        jdk 'JDK17'
    }

    stages {

        stage('Build') {
            steps {
                bat 'mvn clean package -DskipTests'
            }
        }

        stage('Unit Test') {
            steps {
                bat 'mvn test'
            }
        }
    }
}

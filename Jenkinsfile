pipeline {
    agent any

    environment {
        APP_PORT = '9090'
    }

    stages {
        stage('Build') {
            steps {
                bat 'mvn package'
            }
        }

        stage('Unit Test') {
            steps {
                bat 'mvn test'
            }
        }
    }

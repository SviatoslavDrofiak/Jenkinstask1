pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    environment {
        APP_PORT = '9090'
    }

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                bat "mvn clean package"
            }
        }

        stage('Unit Test') {
            steps {
                bat "mvn test"
            }
        }
    }
}

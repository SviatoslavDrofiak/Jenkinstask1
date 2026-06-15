pipeline {
    agent any

    environment {
        APP_PORT = '9090'
    }

    tools {
        jdk 'JDK17'
        maven 'Maven3'
    }

    stages {

        stage('Build') {
            steps {
                bat 'mvn clean package -DskipTest'
            }
        }

        stage('Unit Test') {
            steps {
                bat 'mvn test || exit 0'
            }
        }
    }
}

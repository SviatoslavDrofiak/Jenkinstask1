pipeline {
    agent any

    tools {
        jdk 'JDK17'
        maven 'Maven'
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

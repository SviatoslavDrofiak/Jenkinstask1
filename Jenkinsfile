pipeline {
    agent any

    environment {
        APP_PORT = "9090"
    }

    stages {

        stage('Check Environment') {
            steps {
                sh 'java -version'
                sh 'mvn -v'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package -DskipTests'
            }
        }

        stage('Unit Test') {
            steps {
                sh 'mvn test'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished'
        }
    }
}

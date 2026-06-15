pipeline {
agent any

environment {
    APP_PORT = '9090'
}

stages {
    stage('Build') {
        steps {
            script {

                if (isUnix()) {
                    sh 'mvn clean package -DskipTests'
                } else {
                    bat 'mvn clean package -DskipTests'
                }
            }
        }
    }

    stage('Unit Test') {
        steps {
            script {
                if (isUnix()) {
                    sh 'mvn test'
                } else {
                    bat 'mvn test'
                }
            }
        }
    }
}

}

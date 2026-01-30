pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Compile') {
            steps {
                sh 'javac PrimeNumber.java'
            }
        }

        stage('Run') {
            steps {
                sh 'java PrimeNumber'
            }
        }
    }

    post {
        success {
            echo 'Build Successful!'
        }
        failure {
            echo 'Build Failed!'
        }
    }
}

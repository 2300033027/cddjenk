pipeline {
    agent any

    parameters {
        string(name: 'NUMBER', defaultValue: '7', description: 'Enter number to check')
    }

    stages {

        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Compile') {
            steps {
                bat 'javac PrimeNumber.java'
            }
        }

        stage('Run') {
            steps {
                bat "java PrimeNumber %NUMBER%"
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

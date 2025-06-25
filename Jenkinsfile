pipeline {
    agent any

    stages {
        stage('Checkout the repository') {
            steps {
                checkout scm
            }
        }

        stage('Build the project') {
            steps {
                bat 'dotnet build'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'dotnet test'
            }
        }
    }

    post {
        always {
            echo 'Pipeline Completed'
        }
        success {
            echo 'Build Successful'
        }
        failure {
            echo 'Build Failed'
        }
    }
}
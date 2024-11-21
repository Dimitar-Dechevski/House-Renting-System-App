pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                    git branch: 'main', url: 'https://github.com/Dimitar-Dechevski/House-Renting-System-App.git'
            }
        }
        stage('Restore') {
            steps {
             script {
                    bat "dotnet restore"
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    bat "dotnet build"
                }
            }
        }
        stage('Test') {
            steps {
             script {
                    bat "dotnet test"
                }
            }
        }
    }
    post {
        always {
            echo 'Pipeline execution finished.'
        }
    }
}
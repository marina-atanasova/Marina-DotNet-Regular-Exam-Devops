pipeline {
    agent any

    stages {

        stage('Restore') {
            when {
                branch 'main'
            }
            steps {
                sh 'dotnet restore'
            }
        }

        stage('Build') {
            when {
                branch 'main'
            }
            steps {
                sh 'dotnet build --configuration Release --no-restore'
            }
        }

        stage('Test') {
            when {
                branch 'main'
            }
            steps {
                sh 'dotnet test --configuration Release --no-build'
            }
        }
    }
}

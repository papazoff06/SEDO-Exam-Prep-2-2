pipeline {
    agent any 
    stages {
        stage('Restore .net packages') {
            steps {
                bat 'dotnet restore' //for Win
            }
        }

        stage('Build project') {
            steps {
                bat 'dotnet build --no-restore'
            }
        }

        stage('Test') {
            steps {
                powershell 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}

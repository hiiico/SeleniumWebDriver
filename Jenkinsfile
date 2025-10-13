pipeline {
    agent any
    stages { 
        stage('Restore Project dependences') {
            steps {
                sh 'dotnet restore'
            }
        }
        stage('Build Project') {
            steps {
                sh 'dotnet build --no-restore'
            }
        }
        stage('Run Project 1 Tests') {
            steps {
                sh 'dotnet test TestProject1 --no-build --verbosity normal'
            }
        }
        stage('Run Project 2 Tests') {
            steps {
                sh 'dotnet test TestProject2 --no-build --verbosity normal'
            }
        }
        stage('Run Project 3 Tests') {
            steps {
                sh 'dotnet test TestProject3 --no-build --verbosity normal'
            }
        }
    }
}
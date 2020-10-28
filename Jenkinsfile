pipeline {
    agent none

    stages {
        stage('Build C# code') {
            agent {
                docker { image 'mcr.microsoft.com/dotnet/core/sdk:3.1' }
            }   
            steps {
                echo 'Building..'
                sh 'dotnet build'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
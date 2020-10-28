pipeline {
    agent none

    environment {
        DOTNET_CLI_HOME = "/tmp/DOTNET_CLI_HOME"
    }
    stages {
        stage('Build and test C# code') {
            agent {
                docker { image 'mcr.microsoft.com/dotnet/core/sdk:3.1' }
            }

            stages {

                stage('Build C# code') {
                    steps {
                        echo 'Building C# code..'
                        sh 'dotnet build'
                    }
                }

                stage('Run C# tests') {
                    steps {
                        echo 'Running C# tests'
                        sh 'dotnet test'
                    }     
                }

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
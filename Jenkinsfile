pipeline {
    agent {
        docker { image 'node:14-alpine' }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                // Build the C# code.
                sh 'node --version'
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
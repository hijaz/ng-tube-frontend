pipeline {
    agent any

    stages {
        stage('Install Node.js') {
            steps {
                nvm(version: '16.17.0') {
                    sh 'npm --version'
                    sh 'node --version'
                }
            }
        }

        stage('Install dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
    }
}

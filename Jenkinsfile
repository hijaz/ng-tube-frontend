pipeline {
    agent any

    stages {
        stage('Install Node.js') {
            steps {
                nvm(nodeJSInstallationName: 'Node.js v16.17.0') {
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

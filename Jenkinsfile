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
                withEnv(["PATH+NODE=$NODEJS_HOME/bin"]) {
                    sh 'npm install'
                }
            }
        }

        stage('Build') {
            steps {
                withEnv(["PATH+NODE=$NODEJS_HOME/bin"]) {
                    sh 'npm run build'
                }
            }
        }
    }
}

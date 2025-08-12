pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/akshaya1207/Akshaya_experiment2.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Build') {
            steps {
                bat 'npm run build'
            }
        }

        stage('Run tests') {
            steps {
                bat 'npm test -- --watchAll=false'
            }
        }
    }
}

pipeline {
    agent any

    stages {

        stage('Install & Build') {
            steps {
                dir('frontend') {
                    sh 'npm install'
                    sh 'npm run build'
                }
            }
        }

        stage('Docker Build Frontend') {
            steps {
                sh 'docker build -t frontend-dev ./frontend'
            }
        }
    }
}


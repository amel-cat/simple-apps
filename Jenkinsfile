pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'develop',
                    url: 'https://github.com/amel-cat/simple-apps.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build application'
            }
        }

        stage('Test') {
            steps {
                echo 'Run test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy to Development Server'
            }
        }
    }
}


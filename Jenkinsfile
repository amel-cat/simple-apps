pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                sh '''
                  cd frontend
                  npm install
                '''
            }
        }

        stage('Build Frontend') {
            steps {
                sh '''
                  cd frontend
                  npm run build
                '''
            }
        }
    }
}


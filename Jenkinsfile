pipeline {
    agent any

    environment {
        DEV_HOST = "192.168.77.201"
        DEV_USER = "root"
        APP_DIR  = "/simple-apps"
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Deploy to Dev') {
            steps {
                sh """
                ssh -o StrictHostKeyChecking=no ${DEV_USER}@${DEV_HOST} << EOF
                    cd ${APP_DIR}
                    git pull origin develop
                EOF
                """
            }
        }
    }
}



pipeline {
    agent any

    triggers {
        githubPush()
    }

    environment {
        SSH_USER = "root"
        SSH_HOST = "192.168.77.201"
        SSH_PASS = "123"
        APP_DIR  = "/root/simple-apps"
    }

    stages {
        stage('SSH Git Pull') {
            steps {
                sh """
                sshpass -p '${SSH_PASS}' ssh -o StrictHostKeyChecking=no ${SSH_USER}@${SSH_HOST} "
                    git config --global --add safe.directory ${APP_DIR}
                    cd ${APP_DIR} || exit 1
                    git pull origin develop
                "
                """
            }
        }
    }
}


pipeline {
    agent any
    environment {
        APP_NAME = 'GradeBookApp'
        APP_VERSION = '1.0.0'
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/tanp4577-web/Custom-Environment-Variables-Pipeline.git'
            }
        }
        stage('Show App Info') {
            steps {
                echo "Building ${env.APP_NAME}, version ${env.APP_VERSION}"
            }
        }
        stage('Build') {
            steps {
                bat 'python -m py_compile app.py'
                echo "${env.APP_NAME} version ${env.APP_VERSION} compiled successfully."
            }
        }
    }
}

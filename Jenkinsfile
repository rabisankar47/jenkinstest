pipeline {
    agent any

    environment {
        PYTHON = '"C:/Users/Rabi Sankar Kar/AppData/Local/Programs/Python/Python314/python.exe"'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Setup Python') {
            steps {
                bat "python --version"
            }
        }

        stage('Install Dependancy') {
            steps {
                bat "-pip install -r requirements.txt"
            }
        }

        stage('Extract') {
            steps {
                bat "python extract.py"
            }
        }

        
    }

    post {
        always {
            echo 'Pipeline completed.'
        }
    }
}

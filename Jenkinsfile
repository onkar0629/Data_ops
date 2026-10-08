pipeline {
    agent any

    stages {
        stage('checkout code') {
            steps {
                checkout scm
            }
        }

        stage('run python code') {
            steps {
                sh 'python extract.py'
            }
        }
    }
}
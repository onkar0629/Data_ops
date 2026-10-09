```groovy
pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Create Virtual Environment') {
            steps {
                sh '''
                    python3 -m venv .venv
                    .venv/bin/python -m pip install --upgrade pip
                '''
            }
        }

        stage('Install Dependencies') {
            steps {
                sh '.venv/bin/python -m pip install -r requirements.txt'
            }
        }

        stage('Run Python Code') {
            steps {
                sh '.venv/bin/python extract.py'
            }
        }
    }
}
```
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install requirements') {
            steps {
                sh '''
                    python3 -m pip install --upgrade pip --break-system-packages
                    python3 -m pip install -r requirements.txt --break-system-packages
                '''
            }
        }

        stage('Run Script') {
            steps {
                sh 'python3 app.py'
            }
        }
    }
}

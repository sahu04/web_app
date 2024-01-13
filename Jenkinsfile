pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    // Checkout your Git repository
                    checkout scm
                }
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    // Install required dependencies
                    sh 'pip install --upgrade pip'
                    sh 'pip install -r requirements.txt'
                }
            }
        }

        stage('Deploy to Local Server') {
            steps {
                script {
                    // Your deployment commands
                    sh 'nohup python main.py &'
                    sleep 10  // Give some time for the app to start
                }
            }
        }
    }
}

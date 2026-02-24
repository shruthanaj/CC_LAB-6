pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Cloning repository...'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t backend-image ./backend'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5001:5000 backend-image'
            }
        }
    }
}

pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/AliTalalEl-Abur/tooling.git'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Building project..."'
                sh 'ls -la'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "Running tests..."'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished'
        }
    }
}

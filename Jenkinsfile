pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }

        stage('Deploy to NFS') {
            steps {
                sh '''
                scp -o StrictHostKeyChecking=no README.md ubuntu@54.242.181.160:/mnt/apps/
                '''
            }
        }
    }
}

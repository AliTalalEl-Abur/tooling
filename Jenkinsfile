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
                sshagent(['ec2-ssh']) {
                    sh '''
                    scp -o StrictHostKeyChecking=no README.md ubuntu@18.232.180.194:/mnt/apps/
                    '''
                }
            }
        }
    }
}

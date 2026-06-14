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
                    sh """
                    scp -o StrictHostKeyChecking=no -r * ubuntu@54.242.181.160:/mnt/apps
                    """
                }
            }
        }
    }
}

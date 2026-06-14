pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building...'
            }
        }

        stage('Deploy to EC2') {
            steps {
                sshagent(['ec2-key']) {
                    sh """
                    ssh -o StrictHostKeyChecking=no ubuntu@54.147.138.11 '
                        echo "DEPLOY OK"
                        hostname
                        uptime
                    '
                    """
                }
            }
        }
    }
}

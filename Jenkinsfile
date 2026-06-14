pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/AliTalalEl-Abur/tooling.git'
            }
        }

        stage('Deploy to EC2') {
            steps {
                sshagent(['ec2-ssh']) {
                    sh '''
                    ssh -o StrictHostKeyChecking=no ubuntu@54.147.138.11 "
                        echo 'Deploy OK';
                        hostname;
                        uptime;
                        ls -la
                    "
                    '''
                }
            }
        }
    }
}

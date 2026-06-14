pipeline {
    agent any

    stages {

        stage('Clone repo') {
            steps {
                git 'https://github.com/AliTalalEl-Abur/tooling.git'
            }
        }

        stage('Deploy to EC2') {
            steps {
                sshagent(['ec2-ssh']) {
                    sh '''
                    ssh -o StrictHostKeyChecking=no ubuntu@54.147.138.11 << 'EOF'
                        echo "🚀 Deploy desde Jenkins OK"
                        hostname
                        uptime
                        ls -la
EOF
                    '''
                }
            }
        }
    }
}

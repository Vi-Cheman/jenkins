pipeline {
    agent any
    stages {
        stage('Install Apache2') {
            steps {
                sh '''
                sudo apt update
                sudo apt install -y apache2
                sudo systemctl enable --now apache2
                '''
            }
        }
        stage('Check Apache Status') {
            steps {
                sh 'systemctl status apache2'
            }
        }
    }
}

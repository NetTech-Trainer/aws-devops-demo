pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
                git branch: 'main',
                url: 'https://github.com/NetTech-Trainer/aws-devops-demo.git'
            }
        }
        stage('setup') {
            steps {
                sh '''
                     sudo yum install httpd -y
                     sudo systemctl enable --now httpd
                     '''
            }
        }
        
        stage('deploy') {
            steps {
                sh 'sudo cp -r templatemo_625_folio_slideshow/* /var/www/html/'
            }
        }
        
    }
}

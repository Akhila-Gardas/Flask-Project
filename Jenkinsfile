pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                echo 'Cloning Flask Backend...'
                checkout scm
            }
        }

        stage('Install') {
            steps {
                sh '''
                python3 -m venv venv
                venv/bin/pip install -r requirements.txt
                '''
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                pm2 restart flask || pm2 start app.py --name flask --interpreter ./venv/bin/python
                pm2 save
                '''
            }
        }
    }
}



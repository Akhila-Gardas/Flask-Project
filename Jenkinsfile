pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                echo 'Cloning Express Frontend...'
                checkout scm
            }
        }

        stage('Install') {
            steps {
                sh '''
                npm install
                '''
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                pm2 restart express || pm2 start app.js --name express
                pm2 save
                '''
            }
        }
    }
}

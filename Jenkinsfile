pipeline {
    agent any 
    stages {
        stage('build') {
            steps {
                sh 'npm install'
            }
        }
        stage('test api') {
            steps {
                sh 'npm run webdriver-start & npm run test:local'
            }
        }
        stage('test ui') {
            steps {
                sh 'npm run test:ui:local'
            }
        }
        stage('deploy') {
            steps {
                sh 'sudo /home/ec2-user/.local/bin/eb deploy node-express-env'
            }
        }
    }
    
}
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
                sh 'npm run test:local'
            }
        }
        stage('test ui') {
            steps {
                sh 'npm run test:test:local'
            }
        }
    }
    
}
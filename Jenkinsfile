pipeline {
    agent any 
    stages {
        stage('build') {
            steps {
                sh 'npm install'
            }
        }
    }
    stages {
        stage('test') {
            steps {
                sh 'npm run test:local'
            }
        }
    }
}
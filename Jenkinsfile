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
    }
    
}
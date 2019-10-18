pipeline {
    agent any 
    stages {
        stage('clean all') {
            steps {
                sh 'sudo forever stopall'
            }
        }
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
                sh 'sudo forever start ./bin/www'
            }
        }
    }
    
}
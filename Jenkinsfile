pipeline {
    agent any

    stages {
        stage('test') {
            steps {
                sh 'npm install jest'
                sh 'npm run test'
            }
        }
    }
}
pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git clone 'https://github.com/PrekshaPS04/CI-NODE-APP.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }
        stage('Run Application') {
            steps {
                bat 'node app.js'
            }
        }
        stage('Run Tests') {
            steps {
                bat 'node test.js'
            }
        }
    }
    post{
        success{
            echo 'CI Pipeline Sucess'
        }
        failure{
            echo 'CI Pipeline Failure'
        }
    }
}
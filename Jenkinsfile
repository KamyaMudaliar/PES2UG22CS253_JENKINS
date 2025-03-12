pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                build 'PES2UG22CS253-1'
                sh 'g++ main.cpp -o output'
            }
        }

        stage('Test') {
            steps {
                sh './output'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy' 
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                   
                    sh 'g++ task_55.cpp -o output'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './out'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy :)'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}

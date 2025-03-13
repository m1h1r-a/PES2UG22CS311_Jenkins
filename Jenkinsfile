pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o main/PES2UG22CS311 main/wrong.cpp' 
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './main/PES2UG22CS311' 
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...' 
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}

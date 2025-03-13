pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ PES1UG22CS614.cpp -o PES1UG22CS614'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS614'
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

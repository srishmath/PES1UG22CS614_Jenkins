pipeline {
    agent any

    stages {
        stage('Checkout Main') {
            steps {
                script {
                    checkout([
                        $class: 'GitSCM',
                        branches: [[name: '*/main']],
                        userRemoteConfigs: [[url: 'https://github.com/srishmath/PES1UG22CS614_Jenkins.git']]
                    ])
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    sh 'ls -l'  // Check if .cpp is available
                    sh 'g++ -o PES1UG22CS614-1 PES1UG22CS614.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS614-1'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES1UG22CS614-1 PES1UG22CS614.cpp'  // Compile C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS614-1'  // Run the compiled file
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment stage (placeholder for real deployment)'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}

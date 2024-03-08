pipeline {
    agent any  // Run on any available agent

    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using shell script (replace with your actual command)
                    sh 'g++ helo.cpp -o PES1UG21CS735-1 || echo "Build failed"'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Print output of the compiled program (replace with your actual command)
                    sh './PES1UG21CS735-1 || echo "Test failed"'
                }
            }
        }
        stage('Deploy') {
            // Replace with your actual deployment steps (e.g., copy to server)
            steps {
                script {
                        echo 'Deployment completed!'  // Success message
                }
            }
        }
    }

    // Post-condition: Display "Pipeline failed" on any error
    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}


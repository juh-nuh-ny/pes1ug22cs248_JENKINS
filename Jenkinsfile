pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'g++ main.cpp -o output'   // Compile the C++ file
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'runn ./PES1UG22CS248'  // Run the compiled program
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh 'echo "Deployment successful!"'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'  // Display message on failure
        }
    }
}

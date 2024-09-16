pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                checkout scm
            }
        }

        stage('Run Python Script') {
            steps {
                // Run your Python script
                sh 'python code.py'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed.'
        }
        success {
            echo 'Code ran successfully.'
        }
        failure {
            echo 'Code execution failed.'
        }
    }
}

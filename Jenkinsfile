pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Check out the repository containing the Bash script
                checkout scm
            }
        }
        stage('Set Permissions') {
            steps {
                // Grant execute permission to the Bash script
                sh 'echo i like what i am doing'
            }
        }
        stage('Run Bash Script') {
            steps {
                // Execute the Bash script
                sh 'touch text.txt'
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the logs for details.'
        }
    }
}
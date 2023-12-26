pipeline {
    agent any

    stages {
        stage('Checkout SCM') {
            steps {
                script {
                    checkout scm
                }
            }
        }

        stage('Run Batch Script') {
            steps {
                script {
                    bat 'test.bat' // Use 'bat' instead of 'sh' for Windows
                }
            }
        }
    }
}

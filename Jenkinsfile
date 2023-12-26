pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clean workspace before checkout
                deleteDir()

                // Checkout the source code from your Git repository
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/your-username/your-repo.git']]])
            }
        }

        stage('Run Bash Script') {
            steps {
                // Run the Bash script and capture the output
                def scriptOutput = sh(script: 'chmod +x test.sh && ./test.sh', returnStdout: true).trim()

                // Print the script output
                echo "Script Output: ${scriptOutput}"
            }
        }
    }
}

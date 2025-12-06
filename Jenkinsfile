pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/RareBreedxx/git-practice.git'
            }
        }

        stage('Run System Check') {
            steps {
                // Make script executable
                sh 'chmod +x system_check.sh'
                // Run the script
                sh './system_check.sh'
            }
        }
    }
}


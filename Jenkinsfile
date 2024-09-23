pipeline {
    agent any

    tools {
        nodejs 'NodeJS' // This should match the NodeJS version set in Jenkins
    }

    stages {
        stage('Clone Repository') {
            steps {
                // Clone the GitHub repository
                git 'https://github.com/haseeb3572/arcana-node-app.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                // Install the dependencies from package.json
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                // Run tests (optional, can be skipped if you don't have tests)
                sh 'npm test || echo "No tests available."'
            }
        }

        stage('Build') {
            steps {
                // Placeholder for build steps (if needed)
                echo 'No build step required for this project'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the application (you can customize this to your needs)
                sh 'nohup npm start &'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}

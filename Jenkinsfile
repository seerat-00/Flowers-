pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the React project...'
                script {
                    // Install dependencies and build the project
                    bat 'npm install'    // Use 'bat' for Windows (PowerShell or Command Prompt)
                    bat 'npm run build'
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                script {
                    // Add your testing commands here (e.g., npm test)
                    bat 'npm test'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the React app on Netlify...'
                script {
                    // Add Netlify CLI deployment command or API-based deployment
                    bat 'npx netlify deploy --dir=build --prod'
                }
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}

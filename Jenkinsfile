pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/seerat-00/Flowers-.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the React project...'
                bat 'npm install'
                bat 'npm run build'
            }
        }
        // Other stages...
    }
}

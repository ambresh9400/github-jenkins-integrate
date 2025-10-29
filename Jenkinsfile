pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Pulling code from GitHub...'
                git branch: 'main', url: 'https://github.com/ambresh9400/github-jenkins-integrate.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'echo "Build successful!"'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo "All tests passed!"'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the project...'
                sh 'echo "Deployed successfully!" > /tmp/deploy.txt'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully 🎉'
        }
        failure {
            echo 'Pipeline failed ❌'
        }
    }
}

pipeline {
    agent any

    environment {
        GITHUB_TOKEN = credentials('github-token')
    }

    stages {
        stage('Clone Repository') {
            steps {
                script {
                    git(
                        url: 'https://github.com/zulvit/jenkins_deploy.git',
                        credentials: [username: 'zulvit', password: "${env.GITHUB_TOKEN}"]
                    )
                }
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the project...'
            }
        }
    }
}
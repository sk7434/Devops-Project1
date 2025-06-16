pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/sk7434/Devops-Project1.git'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "No build needed for HTML. Continuing..."'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                    echo "Deploying to Apache server..."
                    sudo mkdir -p /var/www/html/
                    sudo chown -R jenkins:jenkins /var/www/html/
                    cp -r * /var/www/html/
                    echo "Deployment completed."
                '''
            }
        }
    }
}

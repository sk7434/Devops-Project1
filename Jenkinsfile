pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/sk7434/Devops-Project1.git'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Building application..."'
                // For HTML only, no actual build is needed
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

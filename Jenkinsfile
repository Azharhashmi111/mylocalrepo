pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Azharhashmi111/mylocalrepo.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building project...'
                sh 'mvn clean install'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to Tomcat...'
                sh 'cp target/*.war /path/to/tomcat/webapps/'
                sh 'sudo systemctl restart tomcat'
            }
        }
    }}

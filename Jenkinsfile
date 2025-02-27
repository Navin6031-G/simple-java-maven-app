pipeline {
    agent any

    tools {
        maven 'Maven 3'  // Ensure Maven is configured in Jenkins Global Tool Configuration
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url:'https://github.com/Navin6031-G/simple-java-maven-app.git'
            }
        }

        stage('Clean') {
            steps {
                echo 'Running Maven clean...'
                sh 'mvn clean'
            }
        }
    }

    post {
        success {
            echo '✅ Build Successful! Application is ready.'
        }
        failure {
            echo '❌ Build Failed! Check logs.'
        }
    }
}

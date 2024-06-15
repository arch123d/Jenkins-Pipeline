pipeline {
    agent any
    stages {
        stage('Pull') {
            steps {
                git 'https://github.com/sharadrathod/studentapp-ui.git'
                echo '"Pull Successfully"'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
                echo '"Build Successfully"'
                
            }
        }
        stage('Test') {
            steps {
                withSonarQubeEnv(installationName: 'sonar', credentialsId: 'sonar') {
                sh 'mvn sonar:sonar'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo '"Deploy successfully"'
            }
        }
    }
}

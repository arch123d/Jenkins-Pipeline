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
                withSonarQubeEnv(credentialsId: 'sonar') {
            // some block
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

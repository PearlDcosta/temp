pipeline {
    agent any
    stages {
        stage('Fetch') {
            steps {
                echo 'Fetching from Repo'
                git 'https://github.com/PearlDcosta/temp.git'
            }
        }
        stage('build') {
            steps {
                echo 'Building the program'
                bat 'javac Hello.java'
            }
        }
        stage('Execute') {
            steps {
                echo 'Executing'
                bat 'java Hello'
            }
        }
    }
    post{
        success{
            echo 'Pipeline built Successfully'
        }
        failure{
            echo 'Pipeline built failed'
        }
    }
}

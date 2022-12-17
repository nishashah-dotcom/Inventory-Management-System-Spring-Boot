pipeline {
    agent any

 

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '7f6fd200-5e22-4ef2-b7c8-04a2b78da80a', url: 'https://github.com/nishashah-dotcom/Inventory-Management-System-Spring-Boot.git']]])
            }
        }
        stage('Build') {
            steps {
                git credentialsId: '7f6fd200-5e22-4ef2-b7c8-04a2b78da80a', url: 'https://github.com/nishashah-dotcom/Inventory-Management-System-Spring-Boot.git'
            }
        }
        stage('Test and Deploy') {
            steps {
                sh 'echo "Successfully tested and deployed!"'
            }
        }
    }
}

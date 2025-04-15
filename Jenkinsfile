pipeline {
    agent any

    tools {
        maven 'Maven 3.9.9'// Make sure this matches the Maven tool name in Jenkins (Manage Jenkins > Global Tool Configuration)
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/bhu1421/SeleniumTestProject.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean install' // use 'sh' if on a Linux agent
            }
        }

        stage('Run Tests') {
            steps {
                bat 'mvn test'
            }
        }
    }
}

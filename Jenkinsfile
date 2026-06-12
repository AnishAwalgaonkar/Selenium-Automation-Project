pipeline {

    agent any

    tools {

        jdk 'JDK25'

        maven 'Maven-3.9'
    }

    stages {

        stage('Checkout') {

            steps {

                git branch: 'main',
                url: 'https://github.com/AnishAwalgaonkar/Selenium-Automation-Project.git'
            }
        }

        stage('Build') {

            steps {

                bat 'mvn clean test'
            }
        }
    }
}

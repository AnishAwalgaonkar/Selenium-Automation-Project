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

    post {

        always {

            publishHTML([
                allowMissing: true,
                alwaysLinkToLastBuild: true,
                keepAll: true,
                reportDir: 'test-output',
                reportFiles: 'ExtentReport.html',
                reportName: 'Extent Report'
            ])
        }
    }
}

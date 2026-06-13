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
<<<<<<< HEAD
    
=======

>>>>>>> 7a7e81d08ee9949b0597c84414f16da477b7bcae
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
<<<<<<< HEAD
}
=======
}
>>>>>>> 7a7e81d08ee9949b0597c84414f16da477b7bcae

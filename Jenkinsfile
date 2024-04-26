pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building with Maven'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Testing with JUnit, Mockito, and TestNG'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Analysing code with SonarQube'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Security scanning with OWASP ZAP'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging on AWS EC2 with Docker'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Integration testing on staging with Selenium'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production on AWS EC2'
            }
        }
    }

}

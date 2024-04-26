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
            post {
                success {
                    emailext (  
                         to: 'leehoaitram@gmail.com',
                         subject: 'Success: Security Scan Completed',
                         body: 'The security scan completed successfully.',
                         attachLog: true
                        )
                }
                failure {
                    emailext ( 
                         to: 'leehoaitram@gmail.com',
                         subject: 'Failure: Security Scan Failed',
                         body: 'The security scan failed. See attached logs for details.',
                         attachLog: true
                        )
                }
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
            post {
                success {
                    emailext (
                         to: 'leehoaitram@gmail.com',
                         subject: 'Success: Integration Tests on Staging Completed',
                         body: 'Integration Tests on Staging completed successfully.',
                         attachLog: true
                        )
                }
                failure {
                    emailext ( 
                         to: 'leehoaitram@gmail.com',
                         subject: 'Failure: Integration Tests on Staging Failed',
                         body: 'Integration Tests on Staging failed. See attached logs for details.',
                         attachLog: true
                        )
                }
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production on AWS EC2'
            }
        }
    }

}

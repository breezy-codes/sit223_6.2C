pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the code using Maven'
            }
            post {
                failure {
                    mail to: 'breezycodes@gmail.com',
                    subject: 'Failed - Build Status',
                    body: "The build has failed, please check configurations."
                }
                success {
                    mail to: 'breezycodes@gmail.com',
                    subject: 'Success - Build Status',
                    body: "The build has successfully been completed."
                }
            }
        }
        
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running the unit and integration tests using Selenium and JUnit'
            }
            post {
                failure {
                    mail to: 'breezycodes@gmail.com',
                    subject: 'Failed - Unit and Integration Tests',
                    body: "The Unit and Integration Tests has failed, please check configurations."
                }
                success {
                    mail to: 'breezycodes@gmail.com',
                    subject: 'Success - Unit and Integration Tests',
                    body: "The Unit and Integration Tests has successfully been completed."
                }
            }
        }
        
        stage('Code Analysis') {
            steps {
                echo 'Analyzing the code using Jenkins and SonarQube'
            }
        }
        
        stage('Security Scan') {
            steps {
                echo 'Performing a security scan on the code using OWASP ZAP'
            }
            post {
                failure {
                    mail to: 'breezycodes@gmail.com',
                    subject: 'Failed - Security Scan',
                    body: "The Security Scan has failed, please check configurations."
                }
                success {
                    mail to: 'breezycodes@gmail.com',
                    subject: 'Success - Security Scan',
                    body: "The Security Scan has successfully been completed."
                }
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying the application to an AWS EC2 instance'
            }
        }
        
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on the staging environment using Selenium'
            }
            post {
                failure {
                    mail to: 'breezycodes@gmail.com',
                    subject: 'Failed - Integration Tests on Staging',
                    body: "The Integration Tests on Staging has failed, please check configurations."
                }
                success {
                    mail to: 'breezycodes@gmail.com',
                    subject: 'Success - Integration Tests on Staging',
                    body: "The Integration Tests on Staging has successfully been completed."
                }
            }
        }
        
        stage('Deploy to Production') {
            steps {
                echo 'Deploying the application to an AWS EC2 instance'
            }
        }
    }
}

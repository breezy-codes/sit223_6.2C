pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the code using Maven'
            }
            post {
                failure {
                    emailext to: 'breezycodes@gmail.com',
                    attachLog: true,
                    subject: 'Failed - Build Status',
                    body: "The build has failed, please check configurations."
                }
                success {
                    emailext to: 'breezycodes@gmail.com',
                    attachLog: true,
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
                    emailext to: 'breezycodes@gmail.com',
                    attachLog: true,    
                    subject: 'Failed - Unit and Integration Tests',
                    body: "The Unit and Integration Tests has failed, please check configurations."
                }
                success {
                    emailext to: 'breezycodes@gmail.com',
                    attachLog: true,   
                    subject: 'Success - Unit and Integration Tests',
                    body: "The Unit and Integration Tests has successfully been completed."
                }
            }
        }
        
        stage('Code Analysis') {
            steps {
                echo 'Analyzing the code using Jenkins and SonarQube'
            }
            post {
                failure {
                    emailext to: 'breezycodes@gmail.com',
                    attachLog: true,    
                    subject: 'Failed - Code Analysis',
                    body: "The Code Analysis has failed, please check configurations."
                }
                success {
                    emailext to: 'breezycodes@gmail.com',
                    attachLog: true,   
                    subject: 'Success - Code Analysis',
                    body: "The Code Analysis has successfully been completed."
                }
            }
        }
        
        stage('Security Scan') {
            steps {
                echo 'Performing a security scan on the code using OWASP ZAP'
            }
            post {
                failure {
                    emailext to: 'breezycodes@gmail.com',
                    attachLog: true,
                    subject: 'Failed - Security Scan',
                    body: "The Security Scan has failed, please check configurations."
                }
                success {
                    emailext to: 'breezycodes@gmail.com',
                    attachLog: true,
                    subject: 'Success - Security Scan',
                    body: "The Security Scan has successfully been completed."
                }
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying the application to an AWS EC2 instance'
            }
            post {
                failure {
                    emailext to: 'breezycodes@gmail.com',
                    attachLog: true,
                    subject: 'Failed - Deploy to Staging',
                    body: "Deploy to Staging successfully completed."
                }
                success {
                    emailext to: 'breezycodes@gmail.com',
                    attachLog: true,
                    subject: 'Success - Deploy to Staging',
                    body: "Deploy to Staging failed."
                }
            }
        }
        
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on the staging environment using Selenium'
            }
            post {
                failure {
                    emailext to: 'breezycodes@gmail.com',
                    attachLog: true,
                    subject: 'Failed - Integration Tests on Staging',
                    body: "The Integration Tests on Staging has failed, please check configurations."
                }
                success {
                    emailext to: 'breezycodes@gmail.com',
                    attachLog: true,
                    subject: 'Success - Integration Tests on Staging',
                    body: "The Integration Tests on Staging has successfully been completed."
                }
            }
        }
        
        stage('Deploy to Production') {
            steps {
                echo 'Deploying the application to an AWS EC2 instance'
            }
            post {
                failure {
                    emailext to: 'breezycodes@gmail.com',
                    attachLog: true,
                    subject: 'Failed - Deploy to Production',
                    body: "The Deploy to Production has failed, please check configurations."
                }
                success {
                    emailext to: 'breezycodes@gmail.com',
                    attachLog: true,
                    subject: 'Success - Deploy to Production',
                    body: "The Deploy to Production has successfully been completed."
                }
            }
        }
    }
}

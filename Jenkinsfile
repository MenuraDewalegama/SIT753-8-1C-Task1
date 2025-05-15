pipeline {
    agent any
    triggers {
        pollSCM('H/1 * * * *')
    }
    
    stages {
        stage('Build') {
            steps {
                echo "TASK : Compiling the source code to create deployable artifact"
                echo "TOOL : Maven"
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo "TASK : Executes automated tests to ensure the code's functionality"
                echo "TOOL : TestNG"
            }
        }

        stage('Code Analysis') {
            steps {
                echo "TASK : Analyze source code to identify bugs and issues"
                echo "TOOL : SonarQube"
            }
        }

        stage('Security Scan') {
            steps {
                echo "TASK : Scan the source code to identify security vulnerabilities"
                echo "TOOL : Snyk"
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo "TASK : Deploy the application to the further testing"
                echo "TOOL : Ansible"
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo "TASK : Executes automated tests on deployed application"
                echo "TOOL : Selenium"
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "TASK : Deply the application to the live production environment"
                echo "TOOL : AWS CLI"
            }
        } 
    }
}

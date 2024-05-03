pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
              echo "Installing package using npm and building code for node js..."
            }
        }
        stage("Unit and Integration Tests") {
            steps {
              sleep 2
              echo "Running unit tests using Jest"
            }
        }
        stage("Code Analysis") {
            steps {
              sleep 2
              echo "Running code analysis using SonarQube..."
            }
        }
        stage("Security Scan") {
            steps {
              sleep 2
              echo "Performing security scan using OWASP Dependency-Check..."
            }
        }
        stage("Deploy to Staging") {
            steps {
              sleep 2
              echo "Deploying to AWS EC2 instance..."
            }
        }
        stage("Integration Tests on Staging") {
            steps {
              sleep 2
              echo "Running integration tests on staging environment..."
            }
        }
        stage("Deploy to Production") {
            steps {
              sleep 2
              echo "Deploying to production..."
            }
            post {
                success {
                    mail to: "s223606554@deakin.edu.au",
                    subject: "Website Deployment Status",
                    body: "Deployment to production was successful!"
                }
            }
        }
    }
}

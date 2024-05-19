pipeline{
    agent any
    
    stages{
        stage('Build'){
            steps{
                //A tool that could be used: Maven
                echo "Building the code using Maven to compile and package"
            }
        }
        stage('Unit and Integration Tests'){
            steps{
                //A tool that could be used: Unit Tests- TestNG, Integration Tests- Selenium WebDriver
                echo "Running unit tests using TestNG"
                echo "Running integration tests using Selenium WebDriver"
            }
            post{
                success{
                    emailext(
                        to: "amandatse2005@gmail.com",
                        subject: "Unit and Integration Tests Status Email",
                        body: "The unit and integration tests stage was successful!"
                    )
                }
                failure{
                    emailext(
                        to: "amandatse2005@gmail.com",
                        subject: "Unit and Integration Tests Status Email",
                        body: "The unit and integration tests stage was failed!"
                    )
                }
                always {
                    emailext (
                        to: "amandatse2005@gmail.com",
                        subject: "Unit and Integration Tests Status Email",
                        body: "Log attached!",
                        attachLog: true
                    )
                }
            }
        }
        stage('Code Analysis'){
            steps{
                //A tool that could be used: SonarQube
                echo "Analysing the code using SonarQube"
            }
        }
        stage('Security Scan'){
            steps{
                //A tool that could be used: Checkstyle
                echo "Security scanning the code using Checkstyle"
            }
            post{
                success{
                    emailext(
                        to: "amandatse2005@gmail.com",
                        subject: "Security Scan Status Email",
                        body: "The security scan stage was successful!"
                    )
                }
                failure{
                    emailext(
                        to: "amandatse2005@gmail.com",
                        subject: "Security Scan Status Email",
                        body: "The security scan stage was failed!"
                    )
                }
                always {
                    emailext (
                        to: "amandatse2005@gmail.com",
                        subject: "Security Scan Status Email",
                        body: "Log attached!",
                        attachLog: true
                    )
                }
            }
        }
        stage('Deploy to Staging'){
            steps{
                //A tool that could be used: AWS EC2 instance
                echo "Deploying the application to AWS EC2 instance"
            }
        }
        stage('Integration Tests on Staging'){
            steps{
                //A tool that could be used: AWS EC2 instance
                echo "Running integration tests on AWS EC2 instance"
            }
            post{
                success{
                    emailext(
                        to: "amandatse2005@gmail.com",
                        subject: "Integration Tests on Staging Status Email",
                        body: "The integration tests on staging stage was successful!"
                    )
                }
                failure{
                    emailext(
                        to: "amandatse2005@gmail.com",
                        subject: "Integration Tests on Staging Status Email",
                        body: "The integration tests on staging stage was failed!"
                    )
                }
                always {
                    emailext (
                        to: "amandatse2005@gmail.com",
                        subject: "Integration Tests on Staging Status Email",
                        body: "Log attached!",
                        attachLog: true
                    )
                }
            }
        }
        stage('Deploy to Production'){
            steps{
                //A tool that could be used: AWS EC2 instance
                echo "Deploying the application to AWS EC2 instance"
            }
        }
    }
}
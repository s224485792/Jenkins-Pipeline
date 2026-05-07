pipeline {
    agent any 
    
    triggers{
    pollSCM('H/5 * * * *')
}


stages{
    stage('Build') {
        steps{
            echo "building application using npm (javascript)"
        }
    }
    stage('Unit and Intergration Tests'){
        steps{
            echo "Running the unit and integration tests using JUnit"
        }
    }
    stage('Code Analysis'){
        steps{
            echo "Analysing the code using SonarQube"
        }
    }
    stage('Security Scan'){
        steps{
            echo "Performing security scan using OWASP Dependency Check..."
        }
    }
    stage('Deploy to Staging'){
        steps{
            echo "Deploying application using Docker"
        }
    }
    stage('Integration Tests on Staging'){
        steps{
            echo "Running Selenium inetgration tests on staging."
        }
    }
    stage('Deploy to Production'){
        steps{
            echo "Docker system deploys the application to the production"
        }
    }

}
}

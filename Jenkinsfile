pipeline{
    environment {
        registry = 'steevCpp/fastapi-example'
        registryCredential = 'dockerhub-credentials'
        dockerImage = ''
        scannerHome = tool 'SonarQube scanner'
        sonarToken = credentials('credentials-sonar')
        build_version = "1+${BUILD_NUMBER}"
    }
    agent any

    stages {
        stage('Clone github repo'){
            steps {
                git credentialsId: 'github-credentials', url: 'https://github.com/steevCpp/fastapi-examle', branch: 'main'
            }
        }

        stage('Setup') {
            steps {
                sh 'pip install -r requirements.txt --user'
            }
        }

       
        
    }
}



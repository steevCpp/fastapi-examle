pipeline{
    environment {
        registry = 'steevCpp/fastapi-example'
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



pipeline{
    agent any
    stages {
        stage('Clone github repo'){
            steps {
                git credentialsId: 'github-credentials', url: 'https://github.com/kaisbettaieb/fastapi-examle', branch: 'main'

            }
        }

        stage('Setup') {
            steps {
                sh 'pip install -r requirments.txt'
            }
        }

        stage('Unit testin') {
            steps {
                sh 'python -m unittest discover'
            }

        }
    }
}

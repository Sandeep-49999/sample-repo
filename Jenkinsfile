pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Sandeep-49999/sample-repo.git'
            }
        }
        stage('Run Python Script') {
            steps {
                sh 'python3 main.py'
            }
        }
    }
}

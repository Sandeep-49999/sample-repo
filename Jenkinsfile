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
    post{
        success{
            echo "Pipeline is Validated and Successful"
        }
        failure{
            echo "Pipeline execution Failed.Update the Pipeline by checking Error."
        }
    }
            
}

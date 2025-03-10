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
            emailext subject: "Jenkins Build Success ",
                     body: "The Jenkins pipeline executed successfully! ",
                     recipientProviders: [[$class: 'DevelopersRecipientProvider']],
                     to: "samudrala9988@gmail.com"
        }
        failure{
            echo "Pipeline execution Failed.Update the Pipeline by checking Error."
            emailext subject: "Jenkins Build Failed ",
                body: "The Jenkins pipeline Failed! ",
                recipentProviders: [[$class: 'DeveloperRecipientProvider']],
                to: "samudrala9988@gmail.com"
            
        }
    }
            
}

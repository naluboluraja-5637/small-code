pipeline{
    agent any
    stages{
        stage('Clean Workspace') {
            steps {
                deleteDir()
            }
        }
        stage('checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/naluboluraja-5637/small-code.git'
            }
        }
        stage('init'){
            steps{
                sh 'terraform init'
            }
        }
        stage('plan'){
            steps{
                sh 'terraform plan'
            }
        }
        stage('apply'){
            steps{
                sh 'terraform apply -auto-approve'
            }
        }
    }
}

pipeline{
    agent any
    stages{
        stage('Run docker'){
            steps{
                bat 'docker build -t ajay .'
            }
        }
        stage('Run'){
            steps{
                bat 'docker run ajay'
            }
        }
    }
}
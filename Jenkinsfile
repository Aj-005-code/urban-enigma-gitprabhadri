pipeline{
    agent any
    stages{
        stage('Run docker'){
            steps{
                script{
                    try{
                        bat 'docker build -t ajay .'
                    }catch(err){
                        echo "build failed"
                        CurrentBuild.result='FAILURE'
                        error "docker failed to build"
                    }
                }
                
            }
        }
        stage('Run'){
            steps{
                bat 'docker run ajay'
            }
        }
    }
}
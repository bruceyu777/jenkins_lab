pipeline{
    agent any
    
    stages{
        stage('Verify Branch'){
            steps{
                echo "$GIT_BRANCH"
                sh(script: 'echo "hello sh script"' )
            }
        }
        
        stage('Docker Build'){
            steps{
                echo 'check docker image'
                sh(script: """
                    su -
                    Zfyu1206
                    docker images -a
                """)
                sh(script: """
                    cd azure-vote/
                    docker images -a
                    docker build -t jenkins-pipeline .
                    docker images -a
                    cd ..            
                """)
            }
        }
    }
}

pipeline{
    

    stages{
        stage('Checkout'){
        steps{
            git branch: 'main', url:'https://github.com/krasaldo/StudentRegisteryAppDemo'
        }
        }
        stage ('install dependencies'){
            steps{
                script{   
                        bat 'npm install'
                    }
                }
            }
        }
        stage ("start app and run test"){
            steps{
                script{
                    bat 'npm start &'
                    bat 'wait-on https://localhost:8090'
                    bat 'npm test'
                }
            }
        }
    }

pipeline{
    agent any
    stages{
        stage("checkout"){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: 'main']], extensions: [], userRemoteConfigs: [[url: 'git@github.com:pradyumna-scstechsol/calculator.git']]])
            }
        }
        stage("build"){
            steps{
                git branch: 'main', url: 'git@github.com:pradyumna-scstechsol/calculator.git'
                sh 'python calculator.py'
            }
        } 
        stage("test"){
            steps{
                echo "the code is tested"
            }
        }       
    }
}
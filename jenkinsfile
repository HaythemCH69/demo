
pipeline{
    agent any
    stages{
        
        stage('Git Clone'){
            steps{
                sh "rm -rf *"
                git branch: 'main', url: 'https://github.com/HaythemCH69/demo'
            }
        }
        
        stage('Maven Compile'){
            steps{
                sh 'mvn clean compile'
            }
        }
       
        stage('Maven Test'){
            steps{
                sh 'mvn test'
            }
        }
        
        stage('Maven Package'){
            steps{
                sh 'mvn package'
            }
        }
        
        stage('Maven Run'){
            steps{
                sh 'java -jar target/demo-0.1.jar'
            }
        }
       
        stage('Finish'){
            steps{
                echo 'Pipeline terminé'
            }
        }
    }
}

pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       maven 'Maven latest' 
    }
   

    stages{
        stage('build'){
            steps{
                echo 'this is the build job'
                sh 'mvn compile'
            }
        }
        stage('test'){
            steps{
                echo 'this is the test job'
                sh 'test clean'
            }
        }
        stage('package'){
            steps{
                echo 'this is the package job'
                sh 'nvm package -DskipTests'
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}


pipeline{
    agent{docker{image 'node:latest'}}
    stages{
        stage('build'){
             steps{
                 echo "buid"
                 sh "node --version"
             }
        }
        stage('test'){
             steps{
                 echo "test"
             }
        }
    }
    post{
       always{
           echo "i execute always" 
       }
       success{
            echo "i execute success"
       }
       failure{
            echo "i execute failure"
       }
    }
       
    
}

pipeline{
    agent{docker{image 'maven:latest'}}
    stages{
        stage('build'){
             steps{
                 echo "buid"
                 sh "mvn --version"
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

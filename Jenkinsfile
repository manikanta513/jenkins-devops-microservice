pipeline{
    agent any
    environment{
        mavenHome=tool "mymaven"
        dockerHome=tool "mydocker"
        PATH="$mavenHome/bin:$dockerHome/bin:$PATH"
    }
    //agent{docker{image 'node:latest'}}
    stages{
        stage('build'){
             steps{
                 echo "buid"
                 sh "node --version"
                 sh "docker --version"
                 echo "build number: $env.BUILD_NUMBER"
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

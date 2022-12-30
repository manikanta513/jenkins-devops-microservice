pipeline{
    agent any
    environment{
        mavenHome=tool "mymaven"
        dockerHome=tool "mydocker"
        PATH="$mavenHome/bin:$dockerHome/bin:$PATH"
    }
    //agent{docker{image 'node:latest'}}
    stages{
        stage('compile'){
            steps{
                sh "mvn clean compile"
            }
        }
        stage('build'){
             steps{
                 echo "mavenhome - $mavenHome"
                 echo "dockerhome - $dockerHome"
                 echo "build"
                 sh "mvn --version"
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

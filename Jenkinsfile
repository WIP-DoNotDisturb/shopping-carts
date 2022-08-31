pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
   tools{
       maven 'maven' 
    }
  

    stages{
        stage('compile-app'){
            steps{
                echo 'this is the compile job'
                sh 'mvm compile'
            }
        }
        stage('test-app'){
            steps{
                echo 'this is the test job'
                sh 'mvm test'
            }
        }
        stage('package-app'){
            steps{
                echo 'this is the package job'
                sh 'mvm package'
            }
        }
    }
    
    post{
        always{
            echo 'Hurray, my second pipeline is ready!'
        }
        
    }
    


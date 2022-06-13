pipeline{

  //That is mean it is gonna run on any jenkins agnt  
  agent any
  
  
  stages {
  
    stage("build") { 
    
        steps{
          echo 'building step ....' 
          echo 'Build the Application'
        }
      
    }
    
    stage("test"){
    
        steps{
           echo 'testing step ....'
        }
      
    }
    
    stage("deploy"){
    
        steps{
          echo 'deploy step ....'
        }
      
    }
  
  
  }

  post {
    always {
      // This Script will be executed No matter that the build Succ Or Fail  
        echo 'This script execute always ...'
    }
    success {
      echo 'This script execute if the build succeed'
    }
    failure {
      echo 'This script execute if the build fail'
    }
  }

}

//Configure Branch Sources Will Add implicitly A stage whiche Checkout  of code 
//you may send an email to tell the team about the behavior of

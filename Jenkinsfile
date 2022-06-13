pipeline{

  //That is mean it is gonna run on any jenkins agnt  
  agent any
  
  
  stages {
  
    stage("build"){
    
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
}

//Configure Branch Sources Will Add implicitly A stage whiche Checkout  of code 

/* groovylint-disable-next-line CompileStatic */
pipeline {
  //That is mean it is gonna run on any jenkins agnt
  agent any

  environment {
    // defined our v env  that will be available in any stage
    NEW_VERSION = '1.3.0' // calculated or extracted from code
    //Get server Credential to use them in deploy
    SERVER_CREDENTIALS = credential('server-credential')
    //add credential plugin
  }

  stages {
    stage('build') {
        steps {
          echo 'building step ....'
          echo 'Build the Application'
          echo "building version ${NEW_VERSION}"
        }
    }

    stage('test') {
      //This stage will execute only in such branches
      when {
        expression {
          //predefined Env Var
          BRANCH_NAME == 'main'
        }
      }

        steps {
        echo 'testing step ....'
        }
    }

    stage('deploy') {
        steps {
          echo 'deploy step ....'
          echo "deploying with ${SERVER_CREDENTIALS}"
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

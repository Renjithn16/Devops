pipeline {
environment {
    MSBUILD = "C:/Program Files (x86)/Microsoft Visual Studio/2019/Community/MSBuild/Current/Bin/"
    CONFIG = 'Release'
  }
    agent 
    {
        node
        {
         label 'NH00'   
        }
    }
    stages {
    
    stage('Build') {
      steps {
 
        bat """
         "${MSBUILD}MsBuild.exe" DevOps\\DevOps.sln /p:Configuration=${env.CONFIG}
        """
      }
    }
      
    }
   post {
        always {
            emailext body: 'A Test EMail', recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']], subject: 'Test',to:'renjithn16@gmail.com'
        }
    }
}
 

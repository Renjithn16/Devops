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
}
 

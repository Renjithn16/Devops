pipeline {
environment {
    MSBUILD = "C:/Program Files (x86)/Microsoft Visual Studio/2017/BuildTools/MSBuild/15.0/Bin/"
    CONFIG = 'Release'
    PLATFORM = 'x64'
  }
    agent any 
    stages {
    
    stage('Build') {
      steps {
 
        bat """
         "${MSBUILD}MsBuild.exe" DevOps.sln /p:Configuration=${env.CONFIG}
        """
      }
    }
      
    }
}
 

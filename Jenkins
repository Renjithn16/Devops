pipeline {
environment {
    MSBUILD = "C:\Program Files (x86)\Microsoft Visual Studio\2017\BuildTools\MSBuild\15.0\Bin"
    CONFIG = 'Release'
    PLATFORM = 'x64'
  }
    agent any 
    stages {
    
    stage('Build') {
      steps {
        bat "NuGet.exe restore DevOps.sln"
        bat "\"${MSBUILD}\" DevOps.sln /p:Configuration=${env.CONFIG};Platform=${env.PLATFORM} /maxcpucount:%NUMBER_OF_PROCESSORS% /nodeReuse:false"
      }
    }
        stage('Test') { 
            steps {
                // 
            }
        }
        stage('Deploy') { 
            steps {
                // 
            }
        }
    }
}
 

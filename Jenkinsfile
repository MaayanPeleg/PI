pipeline{
  agent any
  
  stages{
    stage('Build Executable'){
      steps{
        sh "chmod 744 algorithm.sh"
      }
    }
    stage('Execute'){
      steps{
        sh "./algorithm.sh"
        archiveArtifacts allowEmptyArchive: true, artifacts: '**/8.txt', fingerprint: true, followSymlinks: false
      }
      
    }
  }
}

pipeline{
  agent any
  
  stages{
    stage('Build Executable'){
      steps{
        sh "chmod 744 pi.sh"
      }
    }
    stage('Execute'){
      steps{
        sh "./pi.sh > output.log"
        archiveArtifacts allowEmptyArchive: true, artifacts: '**/output.log', fingerprint: true, followSymlinks: false
      }
      
    }
  }
}

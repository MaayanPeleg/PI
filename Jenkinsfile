pipeline{
  agent any
  
  stages{
    stage('Build Executable'){
      steps{
        sh "chmod 744 algotithm.sh"
      }
    }
    stage('Execute'){
      steps{
        sh "./algotithm.sh > output.log"
        archiveArtifacts allowEmptyArchive: true, artifacts: '**/output.log', fingerprint: true, followSymlinks: false
      }
      
    }
  }
}

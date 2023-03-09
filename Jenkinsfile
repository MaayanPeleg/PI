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
        sh "./algotithm.sh"
        archiveArtifacts allowEmptyArchive: true, artifacts: '**/8.txt', fingerprint: true, followSymlinks: false
      }
      
    }
  }
}

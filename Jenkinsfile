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
        archiveArtifacts allowEmptyArchive: true, artifacts: '**/*.txt', fingerprint: true, followSymlinks: false
      }
      
    }
  }
}

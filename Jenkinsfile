node {
  stage('build') {
    sh """
      echo "GIT_COMMIT=${GIT_COMMIT}" > build-info.txt
    """
  
    archiveArtifacts artifacts: 'build-info.txt', fingerprint: true
  }
}

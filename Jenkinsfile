stage('build') {
  sh '''
    echo "GIT_COMMIT=${env.GIT_COMMIT}" > build-info.txt
  '''

  archiveArtifacts artifacts: 'build-info.txt', fingerprint: true
}

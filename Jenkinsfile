node {
  stage('build') {
    sh 'env > env.txt'
    readFile('env.txt').split("\r?\n").each {
        println it
    }
    sh """
      echo "GIT_COMMIT=${env.GIT_COMMIT}" > build-info.txt
    """
  
    archiveArtifacts artifacts: 'build-info.txt', fingerprint: true
  }
}

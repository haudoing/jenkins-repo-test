node {
  stage('build') {
    scmVars = checkout(scm: [$class: 'GitSCM', branches: 'main',
                        extensions: scm.extensions])
    sh """
      echo "GIT_COMMIT=${scmVars.GIT_COMMIT}" > build-info.txt
    """
  
    archiveArtifacts artifacts: 'build-info.txt', fingerprint: true
  }
}

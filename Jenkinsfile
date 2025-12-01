node {
  stage('build') {
    scmVars = checkout(scm: [$class: 'GitSCM', branches: [[name:'main']],
                        extensions: scm.extensions,
                        userRemoteConfigs: [[url: 'https://github.com/haudoing/jenkins-repo-test.git']]])
    sh """
      echo "GIT_COMMIT=${scmVars.GIT_COMMIT}" > build-info.txt
    """
  
    archiveArtifacts artifacts: 'build-info.txt', fingerprint: true
  }
}

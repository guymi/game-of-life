pipeline {
  agent {
    node {
        label 'dfi-mac'
        customWorkspace "`dirname $WORKSPACE`/`dirname $JOB_NAME`"
    }
  }
  stages {
    stage('') {
      steps {
        sh 'env'
        sh 'echo hello'
      }
    }

  }
}

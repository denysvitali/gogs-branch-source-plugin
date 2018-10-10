pipeline {
  agent any
  stages {
    stage("Build"){
      steps {
        sh "mvn compile"
      }
    }
  }
  post {
    always {
        archiveArtifacts artifacts: 'target/*.hpi', fingerprint: true
        cleanWs()
    }
  }
}


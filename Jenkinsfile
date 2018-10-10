node {
    try {
        stage ('Checkout'){
            checkout scm
        }

        stage ('Build'){
            sh "mvn compile"
        }
        stage('Archive Artifacts'){
            archiveArtifacts artifacts: "target/*.hpi"
        }
    } finally {
        deleteDir()
    }
}


node {
    try {
        stage ('Checkout'){
            checkout scm
        }

        stage ('Build'){
            sh "mvn package"
        }
        stage('Archive Artifacts'){
            archiveArtifacts artifacts: "target/*.hpi"
        }
    } finally {
        deleteDir()
    }
}


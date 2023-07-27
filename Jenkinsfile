node {
    def mvnHome = tool 'Maven'

    stage('Checkout') {
        checkout scm
    }

    stage('Build') {
        withEnv(["MAVEN_HOME=${mvnHome}"]) {
            sh "${mvnHome}/bin/mvn clean package"
        }
    }
}

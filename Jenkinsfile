#!groovy

node('master') {

try {

    stage('checkout') {
        cleanWs()
        checkout scm
}



}

catch (err) {
    currentBuild.result = "FAILURE"
    throw err
 }

}



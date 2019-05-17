#!groovy

node('master') {

try {

    stage('checkout') {
        cleanWs()
        checkout scm
withCredentials([string(credentialsId: 'Test-text', variable: '')]) {
    // some block
     sh  '''
                vaultpasswordfile="vault_pass.txt"
                echo $Test-text > $vaultpasswordfile
	'''

}


}




}

catch (err) {
    currentBuild.result = "FAILURE"
    throw err
 }

}



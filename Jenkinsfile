#!groovy

node('master') {

try {

    stage('checkout') {
        cleanWs()
        checkout scm
withCredentials([string(credentialsId: 'Test-text', variable: 'vaultpass')]) {
    // some block
     sh  '''
                vaultpasswordfile="vault_pass.txt"
                echo $vaultpass > $vaultpasswordfile
	'''

}


}




}

catch (err) {
    currentBuild.result = "FAILURE"
    throw err
 }

}



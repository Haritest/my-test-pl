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
		cat vault_pass.txt
		pwd
	'''

}


}




}

catch (err) {
    currentBuild.result = "FAILURE"
    throw err
 }

}



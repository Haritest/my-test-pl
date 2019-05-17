#!groovy

node('master') {

try {

    stage('checkout') {
        cleanWs()
        checkout scm
withCredentials([string(credentialsId: 'Test-text', variable: 'vaultpass')]) {
    // some block
     sh  '''
                echo $vaultpass > vault_pass.txt
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



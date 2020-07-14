node {
    stage ('GIT CheckOut') {
        
		sh 'https://github.com/MuraliKarre/Vault.git'
    }
    stage ('Build Artifact') {
	
     sh 'ansible --version'
	 withCredentials([string(credentialsId: 'AnsibleSecret', variable: 'Secret')]) {
   
   
          sh 'ansible-vault view Vaultfile --ask-vault-pass '${Secret}' '
   
   
        }
     	 
    
    
    }
}

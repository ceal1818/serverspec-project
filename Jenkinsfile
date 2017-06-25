#!groovy

node {
   echo "Configurando ambiente..."
   env.PATH = "${env.PATH}"
   
   echo "Obteniendo codigo..."
   checkout scm
    
   sshagent (credentials: ['devops']){
      sh 'SUDO_PASSWORD=servervm rake spec'
   }
}


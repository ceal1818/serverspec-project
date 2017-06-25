#!groovy

node {
   echo "Obteniendo codigo..."
   checkout scm
   sh 'sudo gem install serverspec'   
 
   sshagent (credentials: ['devops']){
      sh 'SUDO_PASSWORD=servervm rake spec'
   }
}


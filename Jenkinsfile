#!groovy

node {

   stage ‘Test’

   echo "Obteniendo codigo..."
   checkout scm
    
   sshagent (credentials: ['devops']){
      sh 'SUDO_PASSWORD=servervm rake spec'
   }
}


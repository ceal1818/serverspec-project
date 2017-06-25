#!groovy

node {


   stage ‘Infraestructure Testing’
   echo "Obteniendo codigo..."
   checkout scm
    
   sshagent (credentials: ['devops']){
      sh 'SUDO_PASSWORD=servervm rake spec'
   }
}


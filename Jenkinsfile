#!groovy

node {
   echo "Obteniendo codigo..."
   checkout scm
   sh 'gem install serverspec'   
 
   sshagent (credentials: ['devops']){
      sh 'SUDO_PASSWORD=servervm rake spec'
   }
}


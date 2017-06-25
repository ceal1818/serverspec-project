#!groovy

node (‘master’){

   stage ‘Infraestructure Testing’
   sshagent (credentials: ['devops']){
      sh 'SUDO_PASSWORD=servervm rake spec'
   }
}


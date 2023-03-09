pipeline {
    agent { lable 'jfrog_1' }
    stages {
        stage('vcs'){
            steps {
               git: 'https://github.com/Shravanipranay/MusicStore.git'
               branch: 'declarative'
            }
        }
        stage('build'){
           steps {
              sh './MusicStore/MusicStore.csproj'
           }

        }
    }   
     
}
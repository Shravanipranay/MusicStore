pipeline {
    agent { label 'jfrog_1' }
    stages {
        stage('vcs'){
            steps {
               git url: 'https://github.com/Shravanipranay/MusicStore.git',
                   branch: 'declarative'
            }
        }
        stage('build'){
           steps {
              sh 'sudo chmod "777" ./MusicStore/MusicStore.csproj'
              sh './MusicStore/MusicStore.csproj'
           }

        }
    }   
     
}
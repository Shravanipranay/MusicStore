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
              sh 'sudo chown ubuntu ./MusicStore/MusicStore.csproj'
              sh 'sudo chgrp ubuntu ./MusicStore/MusicStore.csproj'
              sh './MusicStore/MusicStore.csproj'
           }

        }
    }   
     
}
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
              sh 'dotnet build ./MusicStore/MusicStore.csproj'
           }

        }
        stage('artifacts'){
            steps {
                 archiveArtifacts artifacts : '**/.zip'
            }
        }
    }   
     
}
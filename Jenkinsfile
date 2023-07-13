pipeline {
      agent{ 
        label 'build'
        
    }
// agent any


    stages {

        stage('scm') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], 
                    userRemoteConfigs: [url: 'https://github.com/how2coding/react-nodejs-nginx.git']])
                sh "ls -lst"
            }
        }


        stage('build') {
            steps {
             
               sh "echo build"
            }
            
        }
        
        stage('deploy') {
          
            steps {
               sh "echo deploy"
               
            }
            
        }
    }
}

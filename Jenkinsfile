def myOS = ""
pipeline {
      agent{ 
         label 'build'
        
     }
//agent any

    
    stages {

        stage('scm') {
            steps {
                script {
                    cleanWs()
                    try {
                        sh "ls -lst"
                        myOS="ubuntu"
                    } catch (err) {
                        echo err.getMessage()
                        echo "Error detected, but we will continue."
                        myOS="windows"
                    }
                     echo "========>my os is "+myOS
                   
                    checkout([$class: 'GitSCM', branches: [[name: '*/main']],
                        userRemoteConfigs: [[url: 'https://github.com/how2coding/react-nodejs-nginx.git']]])
                    
                    if(myOS=="ubuntu"){
                        sh "ls -lst"
                    }else{
                        bat 'dir'
                    }
                  
 
                }

            }
        }


        stage('build') {
            steps {
                script {
                    if(myOS=="ubuntu"){
                        sh "docker build -f Dockerfile-prod -t react-nodejs-nginx ."
                    }else{
                        bat 'dir'
                    }

                }
            }
            
        }
        
       
    }
}

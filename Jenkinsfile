def myOS = ""
pipeline {
    //   agent{ 
    //     label 'build'
        
    // }
agent any

    
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

                   
                    // checkout([$class: 'GitSCM', branches: [[name: '*/main']],
                    //     userRemoteConfigs: [[url: 'https://github.com/how2coding/react-nodejs-nginx.git']]])


                    // checkout([$class: 'GitSCM', 
                    // branches: [[name: '*/main']],
                    // doGenerateSubmoduleConfigurations: false,
                    // extensions: [[$class: 'CleanCheckout']],
                    // submoduleCfg: [], 
                    // userRemoteConfigs: [[url: 'https://github.com/how2coding/react-nodejs-nginx.git']]])

                    // git url: 'https://github.com/how2coding/react-nodejs-nginx.git', branch: 'main'
                    // Change file permisson
                    //sh "chmod +x -R ./jenkins"
                    // Run shell script
                    //sh "./jenkins/script/scripted_pipeline_ex_2.sh"
 
                }

            }
        }


        stage('build') {
            steps {
                echo $myOS
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

pipeline {
    //   agent{ 
    //     label 'build'
        
    // }
agent any

     environment {
        OS = ""
    }
    stages {

        stage('scm') {
            steps {
                script {
                    cleanWs()
                    try {
                        sh "ls -lst"
                        AOEU="ubuntu"
                    } catch (err) {
                        echo err.getMessage()
                        echo "Error detected, but we will continue."
                        OS="windows"
                    }

                    echo $OS
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
